# Aplikasi-belajar-ipaexport default function AplikasiBelajar() {
  const materi = [
    {
      judul: "Matematika",
      isi: "Belajar penjumlahan, pengurangan, perkalian, dan pembagian dengan mudah."
    },
    {
      judul: "Bahasa Indonesia",
      isi: "Mengenal huruf, membaca cerita pendek, dan belajar menulis."
    },
    {
      judul: "IPA",
      isi: "Belajar tentang tumbuhan, hewan, dan lingkungan sekitar."
    }
  ];

  return (
    <div className="min-h-screen bg-gradient-to-b from-blue-100 to-purple-100 p-6 font-sans">
      <div className="max-w-5xl mx-auto">
        <div className="bg-white rounded-3xl shadow-xl p-8 text-center">
          <h1 className="text-4xl font-bold text-blue-700 mb-3">
            Aplikasi Belajar Anak
          </h1>
          <p className="text-gray-600 text-lg">
            Belajar jadi lebih menyenangkan dengan materi interaktif.
          </p>

          <button className="mt-6 bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-2xl text-lg shadow-md transition">
            Mulai Belajar
          </button>
        </div>

        <div className="grid md:grid-cols-3 gap-6 mt-10">
          {materi.map((item, index) => (
            <div
              key={index}
              className="bg-white rounded-3xl p-6 shadow-lg hover:scale-105 transition"
            >
              <div className="text-5xl mb-4 text-center">
                {index === 0 ? "📘" : index === 1 ? "✏️" : "🌱"}
              </div>
              <h2 className="text-2xl font-semibold text-purple-700 mb-3 text-center">
                {item.judul}
              </h2>
              <p className="text-gray-600 text-center">{item.isi}</p>
            </div>
          ))}
        </div>

        <div className="bg-white rounded-3xl shadow-xl p-8 mt-10">
          <h2 className="text-3xl font-bold text-center text-blue-700 mb-6">
            Kuis Cepat
          </h2>

          <div className="bg-blue-50 rounded-2xl p-5">
            <p className="text-xl font-medium mb-4">
              Berapa hasil dari 5 + 3?
            </p>

            <div className="grid grid-cols-2 gap-4">
              <button className="bg-white border rounded-xl py-3 hover:bg-blue-100 transition">
                6
              </button>
              <button className="bg-white border rounded-xl py-3 hover:bg-blue-100 transition">
                8
              </button>
              <button className="bg-white border rounded-xl py-3 hover:bg-blue-100 transition">
                9
              </button>
              <button className="bg-white border rounded-xl py-3 hover:bg-blue-100 transition">
                10
              </button>
            </div>
          </div>
        </div>

        <footer className="text-center text-gray-600 mt-10 pb-5">
          © 2026 Aplikasi Belajar Sederhana
        </footer>
      </div>
    </div>
  );
}
