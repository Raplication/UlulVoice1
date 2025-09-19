import React, { useState } from 'react';

const UlulVoiceWebsite = () => {
  const [activeSection, setActiveSection] = useState('home');

  return (
    <div className="min-h-screen bg-background text-foreground font-sans">
      {/* Header */}
      <header className="bg-primary text-primary-foreground py-6 px-4 text-center">
        <h1 className="text-3xl font-bold mb-2">Selamat Datang, Di UlulVoice</h1>
        <p className="text-lg">Bersatu Berkarya, Dan Berprestasi Gemilang</p>
      </header>

      {/* Navigation */}
      <nav className="bg-secondary py-4 px-6 flex justify-center space-x-8">
        <button 
          onClick={() => setActiveSection('home')}
          className={`px-4 py-2 rounded-lg ${activeSection === 'home' ? 'bg-primary text-primary-foreground' : 'hover:bg-accent'}`}
        >
          Tentang OSIS
        </button>
        <button 
          onClick={() => setActiveSection('agenda')}
          className={`px-4 py-2 rounded-lg ${activeSection === 'agenda' ? 'bg-primary text-primary-foreground' : 'hover:bg-accent'}`}
        >
          Agenda Dan Berita
        </button>
        <button 
          onClick={() => setActiveSection('prestasi')}
          className={`px-4 py-2 rounded-lg ${activeSection === 'prestasi' ? 'bg-primary text-primary-foreground' : 'hover:bg-accent'}`}
        >
          Prestasi
        </button>
      </nav>

      {/* Main Content */}
      <main className="container mx-auto px-4 py-8 max-w-4xl">
        {/* Tentang OSIS Section */}
        {activeSection === 'home' && (
          <section className="space-y-6">
            <h2 className="text-2xl font-bold text-center mb-6">Tentang OSIS</h2>
            <div className="bg-muted p-6 rounded-lg">
              <p className="text-foreground leading-relaxed">
                Bersama Osis Smait Ulul Albab, kami membangun pergerakan yang mengedepankan nilai kebersamaan, tanggung jawab, dan profesionalitas. Setiap langkah kami dijiwai oleh karakter Terbaik : Terpercaya, Empati, Religius, Berkomitmen, Aktif, Inovatif, dan Kedisiplinan. Melalui kolaborasi yang solid, kami tidak hanya melanjutkan program yang ada tetapi juga terus berinovasi menciptakan karya baru untuk kemaslahatan bersama.
              </p>
            </div>
          </section>
        )}

        {/* Agenda Dan Berita Section */}
        {activeSection === 'agenda' && (
          <section className="space-y-8">
            <h2 className="text-2xl font-bold text-center mb-6">Agenda Dan Berita</h2>
            <p className="text-center text-muted-foreground mb-8">
              Update kegiatan, acara, dan informasi terbaru Osis Smait Ulul Albab di sini.
            </p>
            
            <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
              {/* Maulid Nabi */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Islamic celebration with students gathered around, decorative banners, and religious atmosphere&id=maulid1&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Kegiatan Maulid Nabi di SMAIT Ulul Albab dengan siswa berkumpul merayakan" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">Maulid Nabi</h3>
                  <p className="text-muted-foreground">
                    Kegiatan maulid nabi di Smait Ulul Albab menjadi momentum penuh makna untuk meneladani akhlak Rasulullah, mempererat ukhuwah, serta menumbuhkan semangat cinta kepada Allah dan rasul-nya.
                  </p>
                </div>
              </div>

              {/* SuperCo */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Students participating in academic competition with focus and determination&id=superco1&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Kegiatan SuperCo dengan siswa berkompetisi dalam suasana akademik" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">SuperCo</h3>
                  <p className="text-muted-foreground">
                    Kompetisi akademik yang menantang kemampuan siswa dalam berbagai bidang ilmu pengetahuan dengan semangat sportivitas dan kejujuran.
                  </p>
                </div>
              </div>

              {/* Study Visual Lanud Anang Busra */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Students visiting air force base with aircraft in background&id=lanud1&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Study visual di Lanud Anang Busra dengan latar belakang pesawat terbang" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">Study Visual Lanud Anang Busra</h3>
                  <p className="text-muted-foreground">
                    Kunjungan edukatif ke Lanud Anang Busra memberikan pengalaman langsung tentang dunia penerbangan dan teknologi kedirgantaraan.
                  </p>
                </div>
              </div>

              {/* Study Visual BMKG */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Students at meteorological agency learning about weather instruments&id=bmkg1&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Study visual di BMKG dengan alat-alat meteorologi dan siswa sedang belajar" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">Study Visual BMKG</h3>
                  <p className="text-muted-foreground">
                    Eksplorasi ilmu cuaca dan iklim di BMKG memperkaya pemahaman siswa tentang fenomena alam dan teknologi prediksi cuaca.
                  </p>
                </div>
              </div>
            </div>
          </section>
        )}

        {/* Prestasi Section */}
        {activeSection === 'prestasi' && (
          <section className="space-y-8">
            <h2 className="text-2xl font-bold text-center mb-6">Prestasi</h2>
            <div className="bg-muted p-6 rounded-lg mb-8">
              <p className="text-foreground leading-relaxed">
                Capaian gemilang Siswa Siswi Smait Ulul Albab, baik dalam bidang akademik maupun non-akademik. setiap prestasi adalah bukti nyata semangat berkarya, berkompetisi, dan berjuang membawa nama baik sekolah. Melalui dokumentasi prestasi ini, diharapkan dapat menjadi motivasi bagi seluruh siswa untuk terus mengembangkan bakat dan meraih pencapaian terbaik di masa depan.
              </p>
            </div>
            
            <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
              {/* Prestasi 1 */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Female taekwondo athlete in uniform with silver medal around neck&id=prestasi1&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Atlet taekwondo perempuan dengan medali perak di leher dan seragam taekwondo" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">Kabar Gembira Ululvers</h3>
                  <p className="text-muted-foreground mb-3">
                    Datang dari salah satu Siswi Terbaik. Rizqya Sainty Aninda yang telah Meraih Prestasi Sebagai Juara 2 (Silver Medal) Poomsae Individual Female Under 17 Year Old ajang bergengsi Kejuaraan Internasional Taekwondo Virtual - World Poomsae Championships Changmookwan 2025.
                  </p>
                  <p className="font-semibold">- Rizqya Sainty Aninda</p>
                </div>
              </div>

              {/* Prestasi 2 */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Student receiving academic award on stage with proud expression&id=prestasi2&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Siswa menerima penghargaan akademik di atas panggung dengan ekspresi bangga" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">Juara Olimpiade Sains Nasional</h3>
                  <p className="text-muted-foreground mb-3">
                    Ahmad Fauzi meraih medali emas dalam Olimpiade Sains Nasional bidang Matematika, membuktikan keunggulan akademik siswa SMAIT Ulul Albab di kancah nasional.
                  </p>
                  <p className="font-semibold">- Ahmad Fauzi</p>
                </div>
              </div>

              {/* Prestasi 3 */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Debate team holding trophy with confident expressions&id=prestasi3&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Tim debat memegang piala dengan ekspresi percaya diri" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">Juara Debat Bahasa Inggris</h3>
                  <p className="text-muted-foreground mb-3">
                    Tim debat SMAIT Ulul Albab sukses menjadi juara pertama dalam kompetisi debat bahasa Inggris se-provinsi, menunjukkan kemampuan komunikasi dan analisis yang luar biasa.
                  </p>
                  <p className="font-semibold">- Tim Debat Bahasa Inggris</p>
                </div>
              </div>

              {/* Prestasi 4 */}
              <div className="bg-card rounded-lg overflow-hidden shadow-md">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Robotics team with their invention at competition&id=prestasi4&customer_id=cus_T4nINh1qfWkHiQ" 
                  alt="Tim robotik dengan penemuan mereka di kompetisi robotika" 
                  className="w-full h-48 object-cover"
                />
                <div className="p-4">
                  <h3 className="font-bold text-lg mb-2">Inovasi Robotika</h3>
                  <p className="text-muted-foreground mb-3">
                    Tim robotik sekolah meraih penghargaan khusus untuk inovasi terbaik dalam kompetisi robotika regional dengan menciptakan robot pembersih lingkungan yang ramah energi.
                  </p>
                  <p className="font-semibold">- Tim Robotika Ulul Albab</p>
                </div>
              </div>
            </div>
          </section>
        )}
      </main>

      {/* Footer */}
      <footer className="bg-primary text-primary-foreground py-6 px-4 text-center mt-8">
        <p>© 2024 UlulVoice.com - OSIS SMAIT Ulul Albab</p>
      </footer>
    </div>
  );
};

export default UlulVoiceWebsite;
