import React from 'react';
import { 
  Search, Menu, Truck, ShieldCheck, 
  Facebook, Instagram, Phone, 
  MessageCircle, Building2, HardHat, 
  MapPin, Target, Eye, Construction, 
  ChevronRight, Clock, CheckCircle2
} from 'lucide-react';

const WHATSAPP_NUMBER = "556234513062";

export default function App() {
  const openWhatsApp = (msg = "Olá! Gostaria de solicitar um orçamento.") => {
    window.open(`https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent(msg)}`, '_blank');
  };

  return (
    <div className="min-h-screen bg-white font-sans text-slate-900 selection:bg-red-100 selection:text-red-600">
      
      {/* Header Fixo */}
      <header className="sticky top-0 z-50 bg-slate-900 text-white shadow-xl">
        <div className="bg-red-600 text-[10px] md:text-xs py-1.5 px-4 text-center font-bold tracking-widest uppercase">
          Referência em Aço e Ferragens • Campos Belos e Região
        </div>
        <div className="container mx-auto px-4 py-4 flex items-center justify-between">
          <div className="flex items-center gap-2">
            <div className="bg-red-500 p-1.5 rounded shadow-lg shadow-red-500/20">
              <HardHat className="w-6 h-6 text-slate-900" />
            </div>
            <div className="flex flex-col leading-none">
              <span className="text-white font-black text-xl tracking-tighter">NACIONAL</span>
              <span className="text-red-500 text-[10px] font-bold tracking-[0.3em] uppercase">Ferragens</span>
            </div>
          </div>
          
          <button 
            onClick={() => openWhatsApp()}
            className="hidden md:flex items-center gap-2 bg-slate-800 hover:bg-slate-700 px-5 py-2.5 rounded-full transition-all border border-slate-700"
          >
            <Phone className="w-4 h-4 text-red-500" />
            <span className="text-xs font-bold uppercase tracking-tight">(62) 3451-3062</span>
          </button>

          <button className="md:hidden text-white">
            <Menu className="w-6 h-6" />
          </button>
        </div>
      </header>

      {/* Hero Section - Impacto Principal */}
      <section className="relative bg-slate-900 pt-20 pb-32 overflow-hidden">
        <div className="absolute inset-0 z-0">
          <img 
            src="https://images.unsplash.com/photo-1504917595217-d4dc5ebe6122?auto=format&fit=crop&q=80&w=2000" 
            alt="Fundo Industrial" 
            className="w-full h-full object-cover opacity-20"
          />
          <div className="absolute inset-0 bg-gradient-to-b from-slate-900/50 via-slate-900 to-slate-900"></div>
        </div>

        <div className="container mx-auto px-4 relative z-10 text-center md:text-left">
          <div className="max-w-3xl animate-fade-in">
            <div className="inline-flex items-center gap-2 bg-red-600/10 border border-red-600/20 px-3 py-1 rounded-full mb-6">
              <span className="relative flex h-2 w-2">
                <span className="animate-ping absolute inline-flex h-full w-full rounded-full bg-red-400 opacity-75"></span>
                <span className="relative inline-flex rounded-full h-2 w-2 bg-red-600"></span>
              </span>
              <span className="text-red-500 text-[10px] font-bold uppercase tracking-wider">Aberto e Pronto para Atender</span>
            </div>
            
            <h1 className="text-4xl md:text-7xl font-black text-white mb-6 leading-[1.1]">
              A Força do Aço para a sua <span className="text-red-600">Obra Não Parar.</span>
            </h1>
            
            <p className="text-slate-400 text-lg md:text-xl mb-10 max-w-2xl leading-relaxed">
              Distribuidora líder em Campos Belos. Especialistas em Aço Gerdau, Metalon, Telhas e Ferramentas Profissionais com entrega imediata.
            </p>

            <div className="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
              <button 
                onClick={() => openWhatsApp()}
                className="group bg-green-600 hover:bg-green-500 text-white font-bold py-5 px-10 rounded-2xl transition-all shadow-2xl shadow-green-600/20 flex items-center justify-center gap-3 text-lg"
              >
                <MessageCircle className="w-6 h-6" />
                Solicitar Orçamento Agora
                <ChevronRight className="w-5 h-5 group-hover:translate-x-1 transition" />
              </button>
              
              <div className="flex items-center justify-center gap-4 px-6 py-4 rounded-2xl bg-white/5 border border-white/10 backdrop-blur-sm text-white/70">
                <Truck className="w-5 h-5 text-red-500" />
                <span className="text-sm font-medium">Frota Própria / Entrega Expressa</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Diferenciais - Grid de Benefícios */}
      <section className="py-24 bg-white relative">
        <div className="container mx-auto px-4">
          <div className="grid md:grid-cols-3 gap-12">
            <div className="flex flex-col items-center text-center group">
              <div className="w-20 h-20 bg-slate-50 rounded-3xl flex items-center justify-center mb-6 group-hover:bg-red-50 transition-colors">
                <ShieldCheck className="w-10 h-10 text-red-600" />
              </div>
              <h3 className="text-xl font-bold mb-3">Qualidade Certificada</h3>
              <p className="text-slate-500 leading-relaxed">Trabalhamos apenas com marcas líderes como Gerdau e ArcelorMittal, garantindo segurança total na sua estrutura.</p>
            </div>

            <div className="flex flex-col items-center text-center group">
              <div className="w-20 h-20 bg-slate-50 rounded-3xl flex items-center justify-center mb-6 group-hover:bg-red-50 transition-colors">
                <Construction className="w-10 h-10 text-red-600" />
              </div>
              <h3 className="text-xl font-bold mb-3">Estoque à Pronta Entrega</h3>
              <p className="text-slate-500 leading-relaxed">Nada de esperar. Nosso pátio conta com amplo estoque de metalon, perfis e telhas para retirada imediata ou entrega.</p>
            </div>

            <div className="flex flex-col items-center text-center group">
              <div className="w-20 h-20 bg-slate-50 rounded-3xl flex items-center justify-center mb-6 group-hover:bg-red-50 transition-colors">
                <Clock className="w-10 h-10 text-red-600" />
              </div>
              <h3 className="text-xl font-bold mb-3">Agilidade no Orçamento</h3>
              <p className="text-slate-500 leading-relaxed">Nossa equipe comercial está pronta para enviar sua cotação completa via WhatsApp em poucos minutos.</p>
            </div>
          </div>
        </div>
      </section>

      {/* Seção Sobre / Localização */}
      <section className="py-24 bg-slate-50">
        <div className="container mx-auto px-4">
          <div className="bg-white rounded-[2rem] overflow-hidden shadow-sm border border-slate-200 flex flex-col md:flex-row">
            <div className="md:w-1/2 p-10 md:p-20 flex flex-col justify-center">
              <h2 className="text-3xl md:text-5xl font-black mb-8 leading-tight">Desde 2016 <span className="text-red-600">construindo</span> parcerias em Goiás.</h2>
              
              <div className="space-y-6 mb-10">
                <div className="flex gap-4">
                  <CheckCircle2 className="w-6 h-6 text-green-500 shrink-0" />
                  <p className="text-slate-600 font-medium">Equipe técnica especializada para indicar o melhor material.</p>
                </div>
                <div className="flex gap-4">
                  <CheckCircle2 className="w-6 h-6 text-green-500 shrink-0" />
                  <p className="text-slate-600 font-medium">Logística eficiente para grandes e pequenas cargas.</p>
                </div>
                <div className="flex gap-4">
                  <CheckCircle2 className="w-6 h-6 text-green-500 shrink-0" />
                  <p className="text-slate-600 font-medium">Preço direto de distribuidora para o consumidor final.</p>
                </div>
              </div>

              <div className="space-y-4">
                <div className="flex items-start gap-4 p-4 rounded-xl bg-slate-50 border border-slate-100">
                  <MapPin className="w-6 h-6 text-red-600 shrink-0" />
                  <div>
                    <h4 className="font-bold">Onde estamos:</h4>
                    <p className="text-sm text-slate-500">Av. GO 118, Qd. QSW3, Lt. 28 - Vila Baiana, Campos Belos - GO</p>
                  </div>
                </div>
              </div>
            </div>
            
            <div className="md:w-1/2 min-h-[400px] relative group">
              <img 
                src="https://images.unsplash.com/photo-1581094794329-c8112a89af12?auto=format&fit=crop&q=80&w=1200" 
                alt="Loja Nacional Ferragens" 
                className="absolute inset-0 w-full h-full object-cover"
              />
              <div className="absolute inset-0 bg-red-600/20 group-hover:bg-red-600/0 transition-all duration-700"></div>
            </div>
          </div>
        </div>
      </section>

      {/* Footer Final */}
      <footer className="bg-slate-900 text-slate-400 py-20 border-t-4 border-red-600">
        <div className="container mx-auto px-4">
          <div className="flex flex-col md:flex-row justify-between items-center gap-12">
            <div className="text-center md:text-left">
              <div className="flex items-center gap-2 mb-4 justify-center md:justify-start">
                <div className="bg-red-500 p-1 rounded">
                  <HardHat className="w-5 h-5 text-slate-900" />
                </div>
                <span className="text-white font-bold text-xl uppercase tracking-tighter">Nacional Ferragens</span>
              </div>
              <p className="max-w-xs text-sm leading-relaxed">
                Referência absoluta em ferragens e aço para construção civil e serralheria em Campos Belos e toda a região.
              </p>
            </div>

            <div className="flex flex-col items-center md:items-end gap-6">
              <div className="flex gap-4">
                <a href="https://www.instagram.com/nacional_ferragens/" target="_blank" className="w-12 h-12 rounded-full bg-slate-800 flex items-center justify-center hover:bg-red-600 hover:text-white transition cursor-pointer">
                  <Instagram className="w-6 h-6" />
                </a>
                <div className="w-12 h-12 rounded-full bg-slate-800 flex items-center justify-center hover:bg-red-600 hover:text-white transition cursor-pointer">
                  <Facebook className="w-6 h-6" />
                </div>
              </div>
              <div className="text-right">
                <p className="text-white font-bold text-lg">(62) 3451-3062</p>
                <p className="text-xs uppercase tracking-widest text-slate-500">Campos Belos - GO</p>
              </div>
            </div>
          </div>
          
          <div className="mt-20 pt-8 border-t border-slate-800 flex flex-col md:flex-row justify-between items-center text-[10px] uppercase tracking-[0.2em] gap-4 text-slate-600 font-bold">
            <p>&copy; 2026 NACIONAL FERRAGENS LTDA. TODOS OS DIREITOS RESERVADOS.</p>
            <p>DESIGN POR GÁSPIO SOLUÇÕES INTELIGÊNTES</p>
          </div>
        </div>
      </footer>

      {/* Botão Flutuante Pulsante do WhatsApp */}
      <button 
        onClick={() => openWhatsApp("Olá! Vi o site e gostaria de um orçamento.")}
        className="fixed bottom-6 right-6 bg-[#25D366] text-white p-4 rounded-full shadow-2xl hover:scale-110 transition-all z-50 group flex items-center gap-2"
      >
        <MessageCircle className="w-8 h-8" />
        <span className="max-w-0 overflow-hidden group-hover:max-w-xs transition-all duration-500 whitespace-nowrap font-bold">Falar no WhatsApp</span>
      </button>

    </div>
  );
}