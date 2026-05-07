import { useState } from "react"


export default function FreeWebsite() {
  const [darkMode, setDarkMode] = useState(false)

  const bgClass = darkMode
    ? "bg-gradient-to-br from-slate-950 via-zinc-900 to-neutral-950 text-white"
    : "bg-gradient-to-br from-slate-100 via-zinc-100 to-neutral-200 text-gray-900"

  return (
    <div className={`min-h-screen overflow-hidden transition-all duration-500 ${bgClass}`}>
      <div className="fixed inset-0 pointer-events-none overflow-hidden z-0">
        <div
          
          
          className="absolute top-10 left-10 w-96 h-96 bg-cyan-400/10 blur-3xl rounded-full animate-pulse"
        />

        <div
          
          
          className="absolute bottom-0 right-0 w-[30rem] h-[30rem] bg-purple-500/10 blur-3xl rounded-full animate-pulse"
        />
      </div>

      <header className="sticky top-0 z-50 backdrop-blur-xl border-b border-cyan-200/10 bg-white/50 dark:bg-zinc-950/40">
        <div className="max-w-7xl mx-auto px-6 py-5 flex justify-between items-center">
          <h1 className="text-3xl font-semibold tracking-tight">
            Asep Gamer Community
          </h1>

          <nav className="hidden md:flex gap-6 text-sm font-medium">
            <a href="https://discord.gg/SkvpUqBh" target="_blank" className="hover:opacity-70 hover:-translate-y-1 transition-all duration-300">Home</a>
            <a href="https://discord.gg/SkvpUqBh" target="_blank" className="hover:opacity-70 hover:-translate-y-1 transition-all duration-300">Games</a>
            <a href="https://discord.gg/SkvpUqBh" target="_blank" className="hover:opacity-70 hover:-translate-y-1 transition-all duration-300">Features</a>
            <a href="https://discord.gg/SkvpUqBh" target="_blank" className="hover:opacity-70 hover:-translate-y-1 transition-all duration-300">Join</a>
          </nav>

          <button
            onClick={() => setDarkMode(!darkMode)}
            className="px-4 py-2 rounded-full bg-gradient-to-r from-cyan-500 to-blue-600 text-white hover:scale-105 hover:shadow-[0_0_40px_rgba(59,130,246,0.45)] transition-all duration-300"
          >
            {darkMode ? "☀ Light" : "🌙 Dark"}
          </button>
        </div>
      </header>

      <section
        id="home"
        className="relative py-36 text-center"
        style={{
          backgroundImage:
            "url('https://images.unsplash.com/photo-1542751110-97427bbecf20?q=80&w=1920&auto=format&fit=crop')",
          backgroundSize: "cover",
          backgroundPosition: "center",
        }}
      >
        <div className="absolute inset-0 bg-black/60" />

        <div
          
          
          
          className="relative z-10 max-w-4xl mx-auto px-6"
        >
          <h2 className="text-5xl md:text-7xl font-bold text-white tracking-tight leading-tight mb-6">
            Level Up Your Gaming Experience
          </h2>

          <p className="text-lg md:text-xl text-stone-200 leading-relaxed max-w-3xl mx-auto">
            Komunitas gamer Indonesia untuk mabar, push rank, tournament, giveaway, dan voice chat aktif setiap hari.
          </p>

          <button
            type="button"
            onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')}
            className="group mt-10 mx-auto flex items-center gap-3 px-8 py-4 rounded-full bg-gradient-to-r from-cyan-500/20 to-purple-500/20 border border-cyan-300/20 text-white backdrop-blur-xl hover:bg-white/20 hover:scale-110 hover:-translate-y-1 transition-all duration-500 shadow-[0_10px_40px_rgba(0,0,0,0.08)] hover:shadow-[0_0_40px_rgba(59,130,246,0.45)]"
          >
            ⭐
            🚀 Join Discord
          </button>
        </div>
      </section>

      <section id="games" className="max-w-7xl mx-auto px-6 py-24">
        <div className="text-center mb-14">
          <h3 className="text-4xl font-semibold tracking-tight mb-4">
            Top Community Games
          </h3>
          <p className={`mb-4 ${darkMode ? 'text-zinc-400' : 'text-zinc-500'}`}>
            Temukan komunitas sesuai game favoritmu dan bermain bersama ribuan gamer aktif setiap hari.
          </p>
          <p className={`${darkMode ? 'text-zinc-300' : 'text-zinc-600'}`}>
            Komunitas aktif untuk berbagai game populer.
          </p>
        </div>

        <div className="grid md:grid-cols-3 gap-8">
          {[
            {
              title: 'Mobile Legends',
              desc: 'Komunitas aktif Mobile Legends untuk push rank, mabar klasik, scrim, dan mencari squad harian.'
            },
            {
              title: 'Free Fire',
              desc: 'Komunitas Free Fire aktif untuk push rank, custom room, turnamen squad, dan mencari teman mabar setiap hari.'
            },
            {
              title: 'Roblox',
              desc: 'Komunitas Roblox aktif untuk bermain berbagai mode game, event komunitas, roleplay, dan mencari teman mabar setiap hari.'
            }
          ].map((game) => (
            <div
              key={game.title}
              onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')}
              
              className={`${darkMode ? 'bg-white/5' : 'bg-white/60'} p-8 rounded-[2rem] backdrop-blur-xl border border-cyan-200/10 shadow-[0_10px_40px_rgba(0,0,0,0.08)] hover:scale-105 hover:-translate-y-2 hover:shadow-[0_0_40px_rgba(59,130,246,0.45)] transition-all duration-500 cursor-pointer`}
            >
              <h4 className="text-2xl font-semibold mb-4">{game.title}</h4>
              <p className={`${darkMode ? 'text-zinc-300' : 'text-zinc-600'}`}>
                {game.desc}
              </p>
            </div>
          ))}
        </div>
      </section>

      <section id="features" className="py-24 px-6">
        <div className="max-w-7xl mx-auto grid md:grid-cols-4 gap-6">
          {[
            {
              title: 'Tournament',
              link: 'https://discord.gg/SkvpUqBh'
            },
            {
              title: 'Voice Chat',
              link: 'https://discord.gg/SkvpUqBh'
            },
            {
              title: 'Leaderboard',
              link: 'https://discord.gg/SkvpUqBh'
            },
            {
              title: 'Giveaway',
              link: 'https://discord.gg/SkvpUqBh'
            }
          ].map((item) => (
            <div
              key={item.title}
              onClick={() => window.open(item.link, '_blank')}
              
              className={`${darkMode ? 'bg-white/5' : 'bg-white/60'} p-6 rounded-[2rem] border border-cyan-200/10 backdrop-blur-xl shadow-[0_10px_30px_rgba(0,0,0,0.08)] hover:scale-105 hover:-translate-y-2 hover:shadow-[0_0_40px_rgba(59,130,246,0.45)] transition-all duration-500 cursor-pointer`}
            >
              <h4 className="text-2xl font-semibold mb-3">⚡ {item.title}</h4>
              <p className={`${darkMode ? 'text-zinc-300' : 'text-zinc-600'}`}>
                Klik untuk bergabung dan melihat informasi lengkap fitur komunitas gamer kami.
              </p>
            </div>
          ))}
        </div>
      </section>

      <section id="join" className="max-w-3xl mx-auto px-6 py-24 text-center">
        <h3 className="text-4xl font-semibold mb-4">Gabung Bersama Ribuan Gamer Aktif</h3>
        <p className={`${darkMode ? 'text-zinc-300' : 'text-zinc-600'} mb-8`}>
          Masuk ke komunitas gaming modern dan temukan teman mabar baru setiap hari.
        </p>

        <form
          
          
          className={`${darkMode ? 'bg-white/5' : 'bg-white/40'} p-8 rounded-[2rem] backdrop-blur-xl border border-cyan-200/10 shadow-[0_10px_40px_rgba(0,0,0,0.08)] space-y-5`}
          onSubmit={(e) => {
            e.preventDefault()
            window.open('https://discord.gg/SkvpUqBh', '_blank')
          }}
        >
          <input
            type="text"
            placeholder="Nama"
            className="w-full p-4 rounded-xl border border-cyan-200/10 bg-white/80 text-black outline-none focus:scale-[1.02] focus:ring-2 focus:ring-cyan-500 transition-all duration-300"
          />

          <input
            type="email"
            placeholder="Email"
            className="w-full p-4 rounded-xl border border-cyan-200/10 bg-white/80 text-black outline-none focus:scale-[1.02] focus:ring-2 focus:ring-cyan-500 transition-all duration-300"
          />

          <textarea
            rows={5}
            placeholder="Game favorit atau pesan"
            className="w-full p-4 rounded-xl border border-cyan-200/10 bg-white/80 text-black outline-none focus:scale-[1.02] focus:ring-2 focus:ring-cyan-500 transition-all duration-300"
          />

          <button className="px-8 py-3 rounded-full bg-gradient-to-r from-cyan-500 to-blue-600 text-white hover:scale-110 hover:-translate-y-1 transition-all duration-300 shadow-[0_10px_30px_rgba(0,0,0,0.08)] hover:shadow-[0_0_40px_rgba(59,130,246,0.45)]">
            🚀 Gabung Sekarang
          </button>
        </form>
      </section>

            <section className="max-w-7xl mx-auto px-6 py-20">
        <div className="grid md:grid-cols-3 gap-8">
          <div
            onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')}
            className={`${darkMode ? 'bg-white/5' : 'bg-white/60'} p-8 rounded-[2rem] border border-cyan-200/10 backdrop-blur-xl shadow-[0_10px_40px_rgba(0,0,0,0.08)] hover:scale-105 hover:-translate-y-2 hover:shadow-[0_0_40px_rgba(59,130,246,0.45)] transition-all duration-500 cursor-pointer`}>
            <h4 className="text-2xl font-semibold mb-4">💎 Experience Gaming Modern</h4>
            <p className={`${darkMode ? 'text-zinc-300' : 'text-zinc-600'} leading-relaxed`}>
              Asep Gamer Community adalah tempat berkumpulnya gamer Indonesia untuk bermain bersama, berbagi tips, dan membangun relasi antar player.
            </p>
          </div>

          <div
            onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')}
            className={`${darkMode ? 'bg-white/5' : 'bg-white/60'} p-8 rounded-[2rem] border border-cyan-200/10 backdrop-blur-xl shadow-[0_10px_40px_rgba(0,0,0,0.08)] hover:scale-105 hover:-translate-y-2 hover:shadow-[0_0_40px_rgba(59,130,246,0.45)] transition-all duration-500 cursor-pointer`}>
            <h4 className="text-2xl font-semibold mb-4">🔥 Kenapa Harus Gabung\?</h4>
            <ul className={`${darkMode ? 'text-zinc-300' : 'text-zinc-600'} space-y-3`}>
              <li onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')} className="cursor-pointer hover:text-cyan-400 transition">• Tournament mingguan</li>
              <li onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')} className="cursor-pointer hover:text-cyan-400 transition">• Giveaway Discord Nitro</li>
              <li onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')} className="cursor-pointer hover:text-cyan-400 transition">• Voice chat 24 jam</li>
              <li onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')} className="cursor-pointer hover:text-cyan-400 transition">• Event mabar harian</li>
            </ul>
          </div>

          <div
            onClick={() => window.open('https://discord.gg/SkvpUqBh', '_blank')}
            className={`${darkMode ? 'bg-white/5' : 'bg-white/60'} p-8 rounded-[2rem] border border-cyan-200/10 backdrop-blur-xl shadow-[0_10px_40px_rgba(0,0,0,0.08)] hover:scale-105 hover:-translate-y-2 hover:shadow-[0_0_40px_rgba(59,130,246,0.45)] transition-all duration-500 cursor-pointer`}>
            <h4 className="text-2xl font-semibold mb-4">⚡ Fitur Eksklusif Komunitas</h4>
            <ul className={`${darkMode ? 'text-zinc-300' : 'text-zinc-600'} space-y-3`}>
              <li>• Member aktif setiap hari</li>
              <li>• Support berbagai game populer</li>
              <li>• Komunitas ramah pemula</li>
              <li>• Server Discord aktif</li>
            </ul>
          </div>
        </div>
      </section>

      <footer className="border-t border-cyan-200/10 bg-white/50 dark:bg-zinc-950/40 backdrop-blur-xl py-8 text-center">
        <button
          onClick={() => window.scrollTo({ top: 0, behavior: 'smooth' })}
          className="mb-4 px-5 py-2 rounded-full bg-gradient-to-r from-cyan-500 to-blue-600 text-white hover:scale-110 hover:-translate-y-1 transition-all duration-300 shadow-[0_10px_30px_rgba(0,0,0,0.08)] hover:shadow-[0_0_40px_rgba(59,130,246,0.45)]"
        >
          ⬆ Kembali ke Atas
        </button>

        <p>© 2026 Asep Gamer Community. Built For Gamers, By Gamers.</p>
      </footer>
    </div>
  )
}
