import React, { useState, useMemo, useEffect } from 'react';
import { 
  Search, 
  Upload, 
  Menu, 
  Home, 
  PlaySquare, 
  ThumbsUp, 
  Share2, 
  CheckCircle2,
  X,
  Play,
  Users,
  Video,
  ChevronLeft,
  Plus,
  FileVideo,
  MessageCircle,
  Send,
  User,
  Camera,
  Edit3,
  ArrowLeft,
  Image as ImageIcon,
  Trash2,
  Save,
  LogOut,
  LayoutGrid
} from 'lucide-react';

/**
 * DATA BRAND DEFAULT
 */
const DEFAULT_BRAND_PHOTO = "Gemini_Generated_Image_xa7arfxa7arfxa7a.png";
const CATEGORIES = ["Semua", "Vlog", "Eksklusif", "Lifestyle", "Tutorial", "Terbaru"];

// URL Gambar Latar Belakang: Siluet wanita gelap
const BG_IMAGE_URL = "https://images.unsplash.com/photo-1509248961158-e54f6934749c?w=1600&q=80";

const INITIAL_VIDEOS = [
  {
    id: '1',
    title: "Momen Spesial: Keseharian di Balik Layar",
    thumbnail: "https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=800&q=80",
    videoUrl: "https://www.w3schools.com/html/mov_bbb.mp4",
    creator: "BbyKhansa",
    creatorPhoto: DEFAULT_BRAND_PHOTO,
    views: "1.2jt",
    timestamp: "2 hari yang lalu",
    category: "Vlog",
    duration: "00:13",
    subscribers: "500rb",
    description: "Halo semua! Video ini adalah rangkuman aktivitas saya minggu ini.",
    likes: 12500,
    comments: [
      { id: 1, user: "Andi", text: "Keren banget kak kontennya!", time: "1 jam yang lalu" }
    ]
  },
  {
    id: '2',
    title: "Tips Produktifitas Untuk Kreator Pemula",
    thumbnail: "https://images.unsplash.com/photo-1498050108023-c5249f4df085?w=800&q=80",
    videoUrl: "https://www.w3schools.com/html/movie.mp4",
    creator: "TechEnthusiast",
    creatorPhoto: "https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?w=400&q=80",
    views: "85rb",
    timestamp: "5 jam yang lalu",
    category: "Tutorial",
    duration: "00:12",
    subscribers: "12rb",
    description: "Bagaimana cara mengatur jadwal konten agar konsisten.",
    likes: 4200,
    comments: []
  }
];

export default function App() {
  const [view, setView] = useState('intro'); 
  const [videos, setVideos] = useState(INITIAL_VIDEOS);
  const [selectedVideo, setSelectedVideo] = useState(null);
  const [searchQuery, setSearchQuery] = useState('');
  const [activeCategory, setActiveCategory] = useState('Semua');
  
  const [userProfile, setUserProfile] = useState({
    name: "Kreator Baru",
    bio: "Selamat datang di channel saya!",
    photo: "https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=400&q=80",
    subscribers: "0"
  });

  const [isSubscribed, setIsSubscribed] = useState(false);
  const [likedVideos, setLikedVideos] = useState(new Set());
  const [editingVideoId, setEditingVideoId] = useState(null);
  const [editTitle, setEditTitle] = useState('');

  const [uploadData, setUploadData] = useState({
    title: '',
    category: 'Vlog',
    description: '',
    videoFile: null,
    videoPreview: null,
    thumbnailPreview: null,
    autoThumbnail: null,
    duration: '00:00' 
  });

  const filteredVideos = useMemo(() => {
    let result = [...videos];
    if (activeCategory !== 'Semua') result = result.filter(v => v.category === activeCategory);
    if (searchQuery) result = result.filter(v => v.title.toLowerCase().includes(searchQuery.toLowerCase()));
    return result;
  }, [activeCategory, searchQuery, videos]);

  const handleVideoChange = (e) => {
    const file = e.target.files[0];
    if (file) {
      const url = URL.createObjectURL(file);
      setUploadData({ ...uploadData, videoFile: file, videoPreview: url });
    }
  };

  const handleUploadSubmit = () => {
    if (!uploadData.title || !uploadData.videoFile) return;
    const newVideo = {
      id: Date.now().toString(),
      title: uploadData.title,
      thumbnail: uploadData.thumbnailPreview || uploadData.autoThumbnail || "https://images.unsplash.com/photo-1593642532400-2682810df593?w=800&q=80",
      videoUrl: uploadData.videoPreview,
      creator: userProfile.name,
      creatorPhoto: userProfile.photo,
      views: "0",
      timestamp: "Baru saja",
      category: uploadData.category,
      duration: uploadData.duration,
      subscribers: userProfile.subscribers,
      description: uploadData.description || "Tidak ada deskripsi.",
      likes: 0,
      comments: []
    };
    setVideos([newVideo, ...videos]);
    setUploadData({ title: '', category: 'Vlog', description: '', videoFile: null, videoPreview: null, thumbnailPreview: null, autoThumbnail: null, duration: '00:00' });
    setView('creator'); 
  };

  const handleDeleteVideo = (id) => {
    setVideos(videos.filter(v => v.id !== id));
  };

  const handleSaveEdit = () => {
    setVideos(videos.map(v => v.id === editingVideoId ? { ...v, title: editTitle } : v));
    setEditingVideoId(null);
  };

  const goHome = () => { setView('home'); setSelectedVideo(null); };

  const Avatar = ({ src, className = "w-10 h-10", onClick }) => (
    <div onClick={onClick} className={`relative flex items-center justify-center bg-sky-50 overflow-hidden rounded-full border border-sky-100 shadow-sm transition-transform hover:scale-105 cursor-pointer ${className}`}>
      <img src={src} alt="User" className="w-full h-full object-cover" onError={(e) => { e.target.src = "https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=400&q=80"; }} />
    </div>
  );

  return (
    <div className="min-h-screen text-slate-900 flex flex-col relative overflow-x-hidden selection:bg-sky-100">
      
      {/* GLOBAL BACKGROUND LAYER - Tetap ada di semua halaman */}
      <div 
        className="fixed inset-0 z-0 pointer-events-none transition-opacity duration-1000"
        style={{ 
          backgroundImage: `url(${BG_IMAGE_URL})`,
          backgroundSize: 'cover',
          backgroundPosition: 'center',
          backgroundAttachment: 'fixed',
          filter: 'grayscale(100%) brightness(15%)',
          opacity: view === 'intro' ? 0.4 : 0.08 // Lebih gelap saat di dalam aplikasi agar tidak mengganggu konten
        }}
      />

      {/* OVERLAY GRADIENT GLOBAL */}
      <div className={`fixed inset-0 z-[1] pointer-events-none transition-colors duration-1000 ${view === 'intro' ? 'bg-slate-900/60' : 'bg-slate-50/90'}`} />

      {/* NAVIGATION BAR - Hanya tampil jika bukan di halaman Intro */}
      {view !== 'intro' && (
        <nav className="fixed top-0 w-full bg-white/70 backdrop-blur-xl border-b border-slate-200/50 z-50 px-6 py-3 flex items-center justify-between">
          <div className="flex items-center gap-3 cursor-pointer group" onClick={goHome}>
            <div className="bg-sky-500 p-1.5 rounded-xl text-white group-hover:scale-110 transition-transform">
              <Video size={20} />
            </div>
            <span className="font-black text-xl tracking-tighter">BbyKhansa</span>
          </div>
          
          {(view === 'home') && (
            <div className="flex-1 max-w-lg mx-8 hidden md:block">
              <div className="relative">
                <input 
                  type="text" placeholder="Cari video creator favoritmu..." 
                  className="w-full bg-slate-200/50 border-none rounded-2xl py-2.5 px-10 focus:ring-2 focus:ring-sky-200 transition-all font-medium"
                  value={searchQuery} onChange={(e) => setSearchQuery(e.target.value)}
                />
                <Search className="absolute left-3 top-3 text-slate-400" size={18} />
              </div>
            </div>
          )}

          <div className="flex items-center gap-4">
            <button 
              onClick={() => setView('upload')} 
              className="hidden sm:flex items-center gap-2 px-4 py-2 bg-sky-500 text-white rounded-xl shadow-lg hover:bg-sky-600 transition-all font-black text-sm"
            >
              <Plus size={18}/> Upload
            </button>
            <div className="h-8 w-px bg-slate-200 hidden sm:block mx-2" />
            <Avatar src={userProfile.photo} onClick={() => setView('profile')} className="w-10 h-10 border-2 border-white shadow-sm" />
            <button onClick={() => setView('intro')} className="p-2 text-slate-400 hover:text-red-500 transition-colors"><LogOut size={20}/></button>
          </div>
        </nav>
      )}

      {/* MAIN CONTENT AREA */}
      <div className={`relative z-10 flex flex-1 ${view !== 'intro' ? 'pt-20' : ''}`}>
        
        {/* SIDEBAR - Hanya tampil di halaman aplikasi tertentu */}
        {view !== 'intro' && (
          <aside className="w-64 fixed left-0 h-[calc(100vh-80px)] p-6 hidden lg:block overflow-y-auto">
            <div className="space-y-2">
              <p className="text-[10px] font-black text-slate-400 uppercase tracking-widest px-4 mb-4">Menu Utama</p>
              <SidebarItem icon={<Home size={20}/>} label="Beranda Video" active={view === 'home' || view === 'watch'} onClick={goHome} />
              <SidebarItem icon={<Users size={20}/>} label="Subscription" active={false} onClick={() => {}} />
              
              <div className="my-8 h-px bg-slate-200/50" />
              
              <p className="text-[10px] font-black text-slate-400 uppercase tracking-widest px-4 mb-4">Fitur Kreator</p>
              <SidebarItem icon={<PlaySquare size={20}/>} label="Dashboard Video" active={view === 'creator'} onClick={() => setView('creator')} />
              <SidebarItem icon={<Upload size={20}/>} label="Upload Konten" active={view === 'upload'} onClick={() => setView('upload')} />
              <SidebarItem icon={<User size={20}/>} label="Profil Saya" active={view === 'profile'} onClick={() => setView('profile')} />
            </div>
          </aside>
        )}

        <main className={`flex-1 transition-all ${view !== 'intro' ? 'lg:pl-64 p-6' : ''}`}>
          
          {/* VIEW: INTRO */}
          {view === 'intro' && (
            <div className="min-h-screen flex items-center justify-center p-6 text-center animate-in fade-in zoom-in duration-700">
              <div className="max-w-md space-y-8">
                <Avatar src={DEFAULT_BRAND_PHOTO} className="w-32 h-32 mx-auto shadow-2xl border-4 border-white/20" />
                <div className="space-y-2">
                  <h1 className="text-4xl font-black text-white tracking-tight drop-shadow-lg">BbyKhansa Platform</h1>
                  <p className="text-slate-300 font-medium">Ruang kreatif untuk inspirasi tanpa batas</p>
                </div>
                <div className="space-y-4">
                  <button onClick={() => setView('home')} className="w-full py-4 bg-white/10 backdrop-blur-md text-white border border-white/20 hover:bg-white hover:text-slate-900 rounded-3xl font-black shadow-lg transition-all flex items-center justify-center gap-3">
                    <Users size={20} /> Masuk sebagai Fans
                  </button>
                  <button onClick={() => setView('profile')} className="w-full py-4 bg-sky-500 hover:bg-sky-600 text-white rounded-3xl font-black shadow-lg transition-all flex items-center justify-center gap-3">
                    <Video size={20} /> Masuk sebagai Kreator
                  </button>
                </div>
              </div>
            </div>
          )}

          {/* VIEW: HOME */}
          {view === 'home' && (
             <div className="max-w-7xl mx-auto space-y-8 animate-in fade-in slide-in-from-bottom-4 duration-500">
                <div className="flex items-center justify-between mb-4">
                  <h1 className="text-2xl font-black text-slate-800">Eksplorasi Video</h1>
                  <div className="flex gap-2 overflow-x-auto no-scrollbar max-w-[60%]">
                    {CATEGORIES.map(c => (
                      <button key={c} onClick={() => setActiveCategory(c)} className={`px-4 py-2 rounded-xl text-[10px] font-black uppercase tracking-wider whitespace-nowrap transition-all ${activeCategory === c ? 'bg-slate-800 text-white shadow-lg' : 'bg-white/50 backdrop-blur-sm border border-slate-200 text-slate-400 hover:bg-white'}`}>{c}</button>
                    ))}
                  </div>
                </div>

                <div className="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-3 gap-8">
                  {filteredVideos.map(v => (
                    <div key={v.id} onClick={() => { setSelectedVideo(v); setView('watch'); }} className="group cursor-pointer space-y-4">
                      <div className="aspect-video rounded-[2.5rem] overflow-hidden bg-slate-200 relative shadow-md transition-all group-hover:-translate-y-2 group-hover:shadow-2xl">
                        <img src={v.thumbnail} className="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110" alt={v.title} />
                        <div className="absolute inset-0 bg-gradient-to-t from-black/40 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                          <div className="bg-white/20 backdrop-blur-md p-4 rounded-full">
                            <Play className="text-white fill-current" size={32} />
                          </div>
                        </div>
                        <div className="absolute bottom-3 right-3 bg-black/60 backdrop-blur-md text-white text-[10px] font-black px-2 py-1 rounded-md">
                          {v.duration || "00:00"}
                        </div>
                      </div>
                      <div className="flex gap-4 px-2">
                        <Avatar src={v.creatorPhoto} className="w-12 h-12 shrink-0 shadow-sm ring-2 ring-white" />
                        <div>
                          <h3 className="font-black text-slate-800 leading-tight line-clamp-2 group-hover:text-sky-600 transition-colors">{v.title}</h3>
                          <div className="flex items-center gap-1 mt-1">
                            <p className="text-xs text-slate-400 font-bold">{v.creator}</p>
                            <CheckCircle2 size={12} className="text-blue-500"/>
                          </div>
                          <p className="text-[10px] text-slate-400 font-bold uppercase tracking-widest mt-0.5">{v.views} Tayangan • {v.timestamp}</p>
                        </div>
                      </div>
                    </div>
                  ))}
                </div>
             </div>
          )}

          {/* VIEW: WATCH */}
          {view === 'watch' && selectedVideo && (
            <div className="max-w-6xl mx-auto space-y-6 animate-in fade-in zoom-in-95 duration-500">
               <button onClick={goHome} className="flex items-center gap-2 font-black text-slate-400 hover:text-slate-800 mb-4 transition-colors">
                  <ArrowLeft size={20}/> Kembali ke Eksplorasi
               </button>
               <div className="aspect-video bg-black rounded-[3rem] overflow-hidden shadow-2xl ring-8 ring-white">
                  <video src={selectedVideo.videoUrl} controls autoPlay className="w-full h-full" />
               </div>
               <div className="bg-white/80 backdrop-blur-xl p-10 rounded-[3rem] shadow-sm border border-slate-200/50 space-y-8">
                  <div className="space-y-2">
                    <span className="px-3 py-1 bg-sky-100 text-sky-600 text-[10px] font-black rounded-full uppercase">{selectedVideo.category}</span>
                    <h1 className="text-3xl font-black text-slate-800 leading-tight">{selectedVideo.title}</h1>
                  </div>

                  <div className="flex flex-col sm:flex-row items-start sm:items-center justify-between gap-6 pb-8 border-b border-slate-200/50">
                    <div className="flex items-center gap-4">
                       <Avatar src={selectedVideo.creatorPhoto} className="w-14 h-14 border-2 border-sky-100" />
                       <div>
                          <p className="font-black text-slate-800 flex items-center gap-1.5 text-lg">
                            {selectedVideo.creator} <CheckCircle2 size={16} className="text-blue-500"/>
                          </p>
                          <p className="text-xs text-slate-400 font-bold uppercase tracking-widest">{selectedVideo.subscribers} Pengikut</p>
                       </div>
                    </div>
                    <button onClick={() => setIsSubscribed(!isSubscribed)} className={`px-8 py-3 rounded-2xl font-black text-xs tracking-widest transition-all ${isSubscribed ? 'bg-slate-200 text-slate-500' : 'bg-sky-500 text-white shadow-xl hover:bg-sky-600'}`}>
                      {isSubscribed ? 'TERDAFTAR' : 'SUBSCRIBE'}
                    </button>
                  </div>

                  <div className="p-8 bg-slate-100/50 rounded-[2rem] border border-slate-200/50">
                    <p className="font-black text-slate-800 mb-2">Deskripsi Video</p>
                    <p className="text-sm font-medium text-slate-500 leading-relaxed">
                      {selectedVideo.description}
                    </p>
                  </div>
               </div>
            </div>
          )}

          {/* VIEW: CREATOR DASHBOARD */}
          {view === 'creator' && (
            <div className="max-w-5xl mx-auto space-y-8 animate-in fade-in duration-500">
               <div className="bg-white/70 backdrop-blur-xl p-8 rounded-[3rem] shadow-sm border border-slate-200/50 flex flex-col md:flex-row md:items-center justify-between gap-6">
                  <div>
                    <h1 className="text-3xl font-black text-slate-800">Dashboard Kreator</h1>
                    <p className="text-slate-400 font-bold">Kelola konten dan interaksi channel Anda.</p>
                  </div>
                  <button onClick={() => setView('upload')} className="bg-sky-500 text-white px-6 py-3 rounded-2xl font-black text-sm shadow-xl hover:bg-sky-600 transition-all flex items-center gap-2">
                    <Upload size={18}/> Video Baru
                  </button>
               </div>

               <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                  {videos.filter(v => v.creator === userProfile.name).map(v => (
                    <div key={v.id} className="bg-white/70 backdrop-blur-xl p-5 rounded-[2.5rem] border border-slate-200/50 shadow-sm flex gap-5 group hover:shadow-xl transition-all">
                       <div className="w-44 aspect-video rounded-2xl overflow-hidden bg-slate-100 shrink-0">
                          <img src={v.thumbnail} className="w-full h-full object-cover" />
                       </div>
                       <div className="flex-1 flex flex-col justify-between py-1">
                          <div>
                            <h3 className="font-black text-slate-800 leading-tight mb-1 line-clamp-2">{v.title}</h3>
                            <span className="bg-slate-100 text-slate-400 text-[9px] font-black px-2 py-0.5 rounded-full uppercase">{v.category}</span>
                          </div>
                          <div className="flex gap-2">
                            <button className="text-[10px] font-black text-sky-500 hover:bg-sky-50 px-3 py-2 rounded-xl transition-colors">Edit</button>
                            <button onClick={() => handleDeleteVideo(v.id)} className="text-[10px] font-black text-red-500 hover:bg-red-50 px-3 py-2 rounded-xl transition-colors">Hapus</button>
                          </div>
                       </div>
                    </div>
                  ))}
               </div>
            </div>
          )}

          {/* VIEW: PROFILE */}
          {view === 'profile' && (
            <div className="max-w-2xl mx-auto space-y-8 animate-in fade-in duration-500">
               <h1 className="text-3xl font-black text-slate-800">Profil Kreator</h1>
               <div className="bg-white/70 backdrop-blur-xl p-12 rounded-[3.5rem] shadow-xl border border-slate-200/50 space-y-10 text-center">
                  <div className="relative w-40 h-40 mx-auto">
                     <Avatar src={userProfile.photo} className="w-full h-full shadow-2xl border-8 border-white ring-1 ring-slate-100" />
                  </div>
                  <div className="space-y-6">
                     <div className="text-left space-y-2">
                        <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest ml-4">Nama Channel</label>
                        <input value={userProfile.name} onChange={(e) => setUserProfile({...userProfile, name: e.target.value})} className="w-full bg-slate-100/50 border-2 border-transparent rounded-2xl p-4 font-black outline-none focus:border-sky-300 transition-all" />
                     </div>
                     <div className="text-left space-y-2">
                        <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest ml-4">Tentang Channel (Bio)</label>
                        <textarea value={userProfile.bio} onChange={(e) => setUserProfile({...userProfile, bio: e.target.value})} className="w-full bg-slate-100/50 border-2 border-transparent rounded-2xl p-4 font-black outline-none h-32 focus:border-sky-300 transition-all" />
                     </div>
                  </div>
                  <button onClick={goHome} className="w-full py-4 bg-slate-800 text-white rounded-2xl font-black shadow-xl hover:bg-slate-900 transition-all">Simpan Perubahan</button>
               </div>
            </div>
          )}

          {/* VIEW: UPLOAD */}
          {view === 'upload' && (
            <div className="max-w-2xl mx-auto bg-white/80 backdrop-blur-xl p-12 rounded-[3.5rem] shadow-2xl space-y-8 animate-in slide-in-from-bottom-8">
               <h2 className="text-2xl font-black tracking-tight">Terbitkan Karya Anda</h2>
               <div className="space-y-6">
                  <div className="relative border-4 border-dashed border-sky-100 rounded-[2.5rem] p-12 text-center bg-sky-50/50 group hover:bg-sky-50 transition-all">
                     <input type="file" accept="video/*" onChange={handleVideoChange} className="absolute inset-0 opacity-0 cursor-pointer" />
                     <div className="space-y-3">
                        <Upload size={28} className="mx-auto text-sky-500" />
                        <p className="text-sm font-black text-slate-800">Klik atau seret file video</p>
                        {uploadData.videoFile && <p className="text-xs font-black text-sky-600">{uploadData.videoFile.name}</p>}
                     </div>
                  </div>
                  <input 
                    placeholder="Judul Video" 
                    className="w-full bg-slate-100/50 border-2 border-transparent rounded-2xl p-4 font-black outline-none focus:border-sky-300 transition-all"
                    value={uploadData.title} onChange={(e) => setUploadData({...uploadData, title: e.target.value})}
                  />
                  <button 
                    disabled={!uploadData.videoFile || !uploadData.title}
                    onClick={handleUploadSubmit}
                    className="w-full py-5 bg-slate-800 text-white rounded-[2rem] font-black shadow-xl hover:bg-slate-900 transition-all disabled:opacity-50"
                  >
                    Publikasikan Sekarang
                  </button>
               </div>
            </div>
          )}

        </main>
      </div>
    </div>
  );
}

function SidebarItem({ icon, label, active, onClick }) {
  return (
    <button 
      onClick={onClick} 
      className={`w-full flex items-center gap-4 px-5 py-4 rounded-[1.5rem] transition-all group ${
        active 
        ? 'bg-slate-900 text-white font-black shadow-xl shadow-slate-200' 
        : 'hover:bg-white text-slate-400 hover:text-sky-500 font-bold'
      }`}
    >
      <div className={`${active ? 'text-sky-400' : 'group-hover:text-sky-500'} transition-colors`}>
        {icon}
      </div>
      <span className="text-sm tracking-tight">{label}</span>
      {active && <div className="ml-auto w-1.5 h-1.5 bg-sky-400 rounded-full" />}
    </button>
  );
}
