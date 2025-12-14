<script lang="ts">
	// Icons
	import { ArrowRight, Plus, ChevronDown, Play } from 'lucide-svelte';

	// State for FAQ
	let openFaq: number | null = null;
	const toggleFaq = (index: number) => {
		openFaq = openFaq === index ? null : index;
	};

	const faqs = [
		{ q: "What sports does Trace support?", a: "Trace is currently available for soccer and basketball, with more sports launching in the future. Our AI technology is continuously learning and expanding to new sports." },
		{ q: "How does the free camera lease work?", a: "Get a free camera lease (normally $495) with an active PlayerFocus subscription. The camera ships within 3 days to U.S. and Canada. As long as you maintain an active subscription, the camera lease is free." },
		{ q: "What's the difference between Basic and Pro?", a: "PlayerFocus Basic ($180/year) includes up to 2 family members and your 5 most recent games. PlayerFocus Pro ($300/year) includes up to 4 family members, all games, full downloads, and player analytics including heatmaps." },
		{ q: "How does PlayerFocus AI work?", a: "Our traceVision AI platform automatically identifies, follows, and spotlights individual players on the field. It creates personalized highlight reels without any manual editing required." },
		{ q: "Do I need to operate the camera during games?", a: "No! Trace is completely autonomous with 'set and forget' operation. Just set up the tripod at the field, and the AI handles everything—tracking players, capturing highlights, and uploading footage automatically." },
		{ q: "Can other families on my team access the footage?", a: "Yes! Other families can join your team roster for free and get free livestream access. They can subscribe to PlayerFocus anytime to get their player's personalized highlights and features." }
	];

    // Generated images - youth sports themed
    const heroImage = "/generated/image-wide-cinematic-shot-of-youth-soccer-game-1765746777807-0.webp"; 
    const soccerGameImage = "/generated/image-parent-filming-youth-soccer-game-from-si-1765746780748-1.webp";
    const playerFocusImage = "/generated/image-youth-soccer-player-dribbling-ball-in-cl-1765746783165-2.webp";
    const multiAngleImage = "/generated/image-wide-angle-view-of-youth-soccer-field-fr-1765746790673-5.webp";
    const cameraEquipment = "/generated/image-professional-sports-camera-mounted-on-ta-1765746802915-10.webp";
    const soccerAction = "/generated/image-youth-soccer-player-running-with-ball-dy-1765746793334-6.webp";
    const basketballAction = "/generated/image-youth-basketball-game-action-player-drib-1765746795638-7.webp";
    const youthSoccer = "/generated/image-young-soccer-player-kicking-ball-intense-1765746785675-3.webp";
    const soccerCelebration = "/generated/image-youth-soccer-team-celebrating-goal-toget-1765746797975-8.webp";
    const highlightSharing = "/generated/image-parent-and-child-watching-sports-highlig-1765746800472-9.webp";
    const aiCamera = "/generated/image-modern-ai-camera-with-sleek-design-on-pr-1765746805527-11.webp";
    const tripodSetup = "/generated/image-professional-16-foot-tripod-with-camera--1765746808038-12.webp";
    const equipmentCase = "/generated/image-protective-black-equipment-case-for-came-1765746810355-13.webp";
    const basketballPlayer = "/generated/image-youth-basketball-player-shooting-layup-i-1765746788121-4.webp";

</script>

<!-- Header -->
<header class="fixed top-0 left-0 right-0 z-50 bg-cream/90 backdrop-blur-sm">
	<div class="container-custom flex items-center justify-between py-4">
	<div class="w-12">
		<button class="w-8 h-8 flex items-center justify-center bg-dark text-white rounded-full">
			<Plus size={20} />
		</button>
	</div>
	<div class="text-sm font-bold tracking-widest uppercase">Trace</div>
	<div class="w-12 flex justify-end">
		<button class="text-xs font-medium border border-gray-300 rounded-full px-3 py-1 hover:bg-gray-100">EN</button>
	</div>
	</div>
</header>

<main class="pt-24">
	<!-- Hero Section -->
	<section class="container-custom py-16">
		<div class="flex flex-col items-center text-center mb-8">
			<p class="text-xs text-gray-500 mb-3 max-w-xs">AI-powered sports filming<br>for youth athletes</p>
			<h1 class="text-6xl md:text-8xl font-medium tracking-tight">All Your Angles</h1>
		</div>

		<div class="relative w-full aspect-[16/9] md:aspect-[21/9] rounded-3xl overflow-hidden mb-8 bg-gray-200">
			<img src={heroImage} alt="Youth soccer game in action" class="w-full h-full object-cover" />
		</div>

		<div class="max-w-3xl mx-auto text-center">
			<p class="text-xl md:text-2xl leading-relaxed font-light text-gray-800">
				Trace transforms youth sports filming into player-focused highlights via autonomous AI camera tracking. Never miss a moment—our AI captures every play, follows your player, and creates personalized highlight reels automatically.
			</p>
		</div>
	</section>

	<!-- Story / Video Section -->
	<section class="container-custom py-16">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
			<div class="max-w-sm">
				<p class="text-sm leading-relaxed text-gray-600">
					Parents shouldn't have to choose between watching the game and filming it. See how Trace is revolutionizing youth sports memories with AI-powered player tracking.
				</p>
			</div>
			<div class="relative aspect-video rounded-xl overflow-hidden bg-gray-800 group cursor-pointer">
				<img src={soccerGameImage} alt="Video thumbnail" class="w-full h-full object-cover opacity-80 group-hover:opacity-60 transition-opacity" />
				<div class="absolute inset-0 flex items-center justify-center">
					<div class="w-12 h-12 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
						<Play size={20} fill="currentColor" />
					</div>
				</div>
				<div class="absolute bottom-4 left-4 text-white text-sm font-medium">01. How Trace works</div>
			</div>
		</div>
	</section>

	<!-- Typography Section -->
	<section class="container-custom py-16">
		<div class="flex flex-col text-7xl md:text-9xl font-medium tracking-tighter leading-none mb-8">
			<span class="self-start">Every</span>
			<span class="self-center my-4 md:my-8">play</span>
			<span class="self-end">captured</span>
		</div>

		<div class="max-w-2xl mx-auto text-center">
			<p class="text-lg text-gray-600 leading-relaxed">
				Powered by traceVision, the most advanced AI vision platform for sports. Our PlayerFocus AI automatically identifies, follows, and spotlights individual players—creating personalized highlight reels without any manual editing.
			</p>
		</div>
	</section>

	<!-- Feature 1: PlayerFocus AI -->
	<section class="container-custom py-16">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-6 group">
			<img src={playerFocusImage} alt="PlayerFocus AI tracking player" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">PlayerFocus AI</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Your player, automatically spotlighted</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end">
				<p class="text-sm text-gray-600 leading-relaxed max-w-xs">
					PlayerFocus AI automatically identifies and follows your player throughout the entire game. Get a 4x zoomed PlayerCam view that keeps your athlete in focus, plus auto-tagged plays and timeline highlights for easy navigation to key moments.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden">
				<img src={youthSoccer} alt="Player tracking in action" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. AI player identification</div>
			</div>
		</div>
	</section>

	<!-- Feature 2: Multiple Angles -->
	<section class="container-custom py-16">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-6 group">
			<img src={multiAngleImage} alt="Multiple camera angles" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">All Your Angles,<br>One Camera</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">PlayerCam, TraceCam, and MultiCam views</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					Experience the game from every perspective. PlayerCam gives you a 4x zoom on your athlete. TraceCam provides tactical full-field coverage. MultiCam integrates smartphones for position-specific angles. All from a single 180-degree camera setup.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={soccerAction} alt="PlayerCam view" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. PlayerCam 4x zoom</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={basketballAction} alt="TraceCam view" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. Full-field TraceCam</div>
			</div>
		</div>
	</section>

	<!-- Feature 3: Instant Highlights -->
	<section class="container-custom py-16">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-6 group">
			<img src={soccerCelebration} alt="Instant highlights" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Lightning-fast highlights</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Share the best moments instantly</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					Over one million highlights added to our platform regularly. AI-generated game recaps, auto-tagged plays, and instant reel creation mean you can share your player's best moments with family, friends, and recruiters within minutes of the final whistle.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src="https://images.unsplash.com/photo-1431324155629-1a6deb1dec8d?q=80&w=2670&auto=format&fit=crop" alt="Highlight reel" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Auto-generated recaps</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src="https://images.unsplash.com/photo-1560272564-c83b66b1ad12?q=80&w=2670&auto=format&fit=crop" alt="Share highlights" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. Share with recruiters</div>
			</div>
		</div>
	</section>

	<!-- Technology Section (Sage Green) -->
	<section class="bg-sage py-16">
		<div class="container-custom">
			<div class="flex flex-col items-center text-center">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight text-white mb-8 drop-shadow-sm">Powered by traceVision</h2>

				<div class="relative w-full max-w-4xl aspect-square md:aspect-[16/9] mb-8">
					<img src={cameraEquipment} alt="Trace camera equipment" class="w-full h-full object-contain mix-blend-multiply" />
				</div>

				<div class="max-w-2xl mx-auto mb-8">
					<p class="text-xl text-gray-700 leading-relaxed">
						The most advanced AI vision platform for sports. traceVision powers PlayerFocus AI to automatically identify, track, and spotlight individual players across thousands of games filmed weekly.
					</p>
				</div>

				<div class="relative w-full max-w-3xl aspect-video rounded-2xl overflow-hidden mb-8 bg-gray-800">
					<img src={playerFocusImage} alt="Video thumbnail" class="w-full h-full object-cover opacity-80" />
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="w-16 h-16 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
							<Play size={24} fill="currentColor" />
						</div>
					</div>
					<div class="absolute bottom-4 left-4 text-white text-xs font-medium">01. traceVision AI in action</div>
				</div>

				<div class="text-center max-w-md mx-auto text-sm text-gray-600 mb-4">
					Over one million highlights created. Thousands of games filmed weekly. Trace is revolutionizing how youth athletes capture and share their sports journey.
				</div>

				<div class="flex gap-8 justify-center text-sm font-medium">
					<a href="#" class="border-b border-gray-400 pb-0.5 hover:border-black transition-colors">Explore Technology</a>
					<a href="#" class="border-b border-gray-400 pb-0.5 hover:border-black transition-colors">Get Started</a>
				</div>
			</div>
		</div>
	</section>

	<!-- Design Section -->
	<section class="py-16 bg-cream">
		<div class="container-custom">
			<div class="text-center mb-12">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight mb-6">Built for the<br>sidelines</h2>
				
				<div class="inline-flex bg-white rounded-full p-1 shadow-sm border border-gray-100">
					<button class="px-6 py-2 rounded-full bg-gray-100 text-sm font-medium">Equipment</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Setup</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Features</button>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
				<!-- Card 1 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden group">
					<img src={soccerAction} alt="180-degree coverage" class="w-full h-full object-cover" />
					<div class="absolute inset-0 bg-black/40 p-8 flex flex-col justify-between opacity-0 group-hover:opacity-100 transition-opacity duration-300">
						<div class="text-white">
							<h3 class="font-bold mb-2">180° field coverage</h3>
							<p class="text-xs leading-relaxed opacity-90">One camera captures the entire field with our advanced 180-degree lens system. No blind spots, no missed plays.</p>
						</div>
					</div>
				</div>

				<!-- Card 2 -->
				<div class="bg-[#e8e4dc] rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">Set and forget operation</h3>
					<p class="text-sm text-gray-600 leading-relaxed">
						Autonomous AI tracking means you just set up the tripod and let Trace do the work. Watch the game, not the camera.
					</p>
				</div>

				<!-- Card 3 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden bg-dark">
					<img src={cameraEquipment} alt="Equipment" class="w-full h-full object-cover mix-blend-lighten opacity-60" />
                    <div class="absolute bottom-8 right-8 w-12 h-12 bg-white rounded-full flex items-center justify-center text-dark">
                        <Plus size={20} />
                    </div>
				</div>

                <!-- Card 4 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden">
					<img src="https://images.unsplash.com/photo-1606925797300-0b35e9d1794e?q=80&w=2670&auto=format&fit=crop" alt="Tripod setup" class="w-full h-full object-cover" />
                    <div class="absolute top-8 left-8 text-white max-w-[200px]">
                        <h3 class="font-bold text-sm mb-1">Professional 16ft tripod</h3>
                        <p class="text-[10px] opacity-80">Includes 3 sandbags for stability in any weather condition.</p>
                    </div>
				</div>

                 <!-- Card 5 -->
				<div class="bg-[#dce3de] rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">Fast upload, instant access</h3>
					<p class="text-sm text-gray-600 leading-relaxed">
						Built-in fast uploading means highlights are ready to view and share within minutes of the game ending.
					</p>
				</div>

                 <!-- Card 6 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden">
					<img src={equipmentCase} alt="Protective case" class="w-full h-full object-cover" />
				</div>
			</div>
		</div>
	</section>

	<!-- Pricing Section (Sky Blue) -->
	<section class="bg-sky py-16">
		<div class="container-custom flex flex-col items-center text-center">
			<h2 class="text-4xl md:text-6xl font-medium tracking-tight mb-6">Choose your plan</h2>
			<p class="text-lg text-gray-600 mb-10 max-w-2xl">Free camera lease with active subscription. Start capturing every moment today.</p>

			<div class="grid grid-cols-1 md:grid-cols-2 gap-6 w-full max-w-4xl mb-6">
				<!-- Basic Plan -->
				<div class="bg-white rounded-3xl p-8 text-left">
					<h3 class="text-2xl font-medium mb-2">PlayerFocus Basic</h3>
					<div class="text-4xl font-bold mb-4">$180<span class="text-lg font-normal text-gray-500">/year</span></div>
					<ul class="space-y-3 text-sm text-gray-600 mb-8">
						<li class="flex items-start"><span class="mr-2">✓</span> Up to 2 family members</li>
						<li class="flex items-start"><span class="mr-2">✓</span> 5 most recent games</li>
						<li class="flex items-start"><span class="mr-2">✓</span> PlayerCam & TraceCam views</li>
						<li class="flex items-start"><span class="mr-2">✓</span> Auto-generated highlights</li>
						<li class="flex items-start"><span class="mr-2">✓</span> Free livestream access</li>
					</ul>
					<button class="w-full bg-dark text-white px-6 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
						Get Started
					</button>
				</div>

				<!-- Pro Plan -->
				<div class="bg-dark text-white rounded-3xl p-8 text-left relative overflow-hidden">
					<div class="absolute top-4 right-4 bg-white text-dark text-xs font-bold px-3 py-1 rounded-full">POPULAR</div>
					<h3 class="text-2xl font-medium mb-2">PlayerFocus Pro</h3>
					<div class="text-4xl font-bold mb-4">$300<span class="text-lg font-normal text-gray-300">/year</span></div>
					<ul class="space-y-3 text-sm text-gray-300 mb-8">
						<li class="flex items-start"><span class="mr-2">✓</span> Up to 4 family members</li>
						<li class="flex items-start"><span class="mr-2">✓</span> All games saved</li>
						<li class="flex items-start"><span class="mr-2">✓</span> All camera angles + MultiCam</li>
						<li class="flex items-start"><span class="mr-2">✓</span> Full game downloads</li>
						<li class="flex items-start"><span class="mr-2">✓</span> Player heatmaps & analytics</li>
						<li class="flex items-start"><span class="mr-2">✓</span> Trace iD public profile</li>
					</ul>
					<button class="w-full bg-white text-dark px-6 py-3 rounded-full text-sm font-medium hover:bg-gray-100 transition-colors">
						Get Started
					</button>
				</div>
			</div>

			<p class="text-sm text-gray-600">Team pricing unlocks when 7+ families subscribe. <a href="#" class="underline">Learn more</a></p>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="py-16 container-custom">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<div>
				<h2 class="text-sm font-medium text-gray-500 uppercase tracking-wide">Frequently asked questions</h2>
			</div>
			<div class="md:col-span-2">
				<div class="space-y-4">
					{#each faqs as faq, i}
						<div class="border-b border-gray-200 pb-4">
							<button 
								class="w-full flex items-center justify-between text-left py-4 focus:outline-none group"
								onclick={() => toggleFaq(i)}
							>
								<span class="text-lg font-medium group-hover:text-gray-600 transition-colors">{faq.q}</span>
								<ChevronDown class="transition-transform duration-300 {openFaq === i ? 'rotate-180' : ''}" />
							</button>
							{#if openFaq === i}
								<div class="pb-4 text-gray-600 leading-relaxed">
									{faq.a}
								</div>
							{/if}
						</div>
					{/each}
				</div>
			</div>
		</div>
	</section>
</main>

<!-- Footer -->
<footer class="bg-neon-yellow pt-16 pb-8 rounded-t-[3rem] mt-[-2rem] relative z-10">
	<div class="container-custom">
		<!-- Black CTA Box -->
		<div class="bg-dark text-white rounded-3xl p-10 md:p-14 text-center mb-16 relative overflow-hidden">
			<div class="relative z-10">
				<h2 class="text-2xl md:text-4xl font-medium mb-6">Ready to capture every moment? <span class="text-gray-400">Free camera lease. Ships in 3 days.</span></h2>
				<a href="#" class="inline-flex items-center border border-white/30 rounded-full px-6 py-2 hover:bg-white/10 transition-colors text-sm">
					Get Started <ArrowRight size={16} class="ml-2" />
				</a>
			</div>
		</div>

		<!-- Footer Links -->
		<div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-12 text-sm">
			<div class="col-span-2 md:col-span-1">
				<p class="mb-4">Get the latest news</p>
				<form class="flex border-b border-black pb-2">
					<input type="email" placeholder="Email address" class="bg-transparent border-none outline-none w-full placeholder-gray-600" />
					<button type="submit" class="font-medium">Subscribe</button>
				</form>
			</div>
			
			<div class="md:col-start-3">
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">How It Works</a></li>
					<li><a href="#" class="hover:underline">Technology</a></li>
					<li><a href="#" class="hover:underline">Pricing</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">For Teams</a></li>
					<li><a href="#" class="hover:underline">For Clubs</a></li>
					<li><a href="#" class="hover:underline">Support</a></li>
					<li><a href="#" class="hover:underline">FAQ</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">Facebook</a></li>
					<li><a href="#" class="hover:underline">Instagram</a></li>
					<li><a href="#" class="hover:underline">YouTube</a></li>
					<li><a href="#" class="hover:underline">X (Twitter)</a></li>
				</ul>
			</div>
		</div>

		<!-- Bottom Bar -->
		<div class="flex flex-col md:flex-row justify-between items-center text-[10px] uppercase tracking-wider text-gray-800 border-t border-black/10 pt-8">
			<div class="mb-4 md:mb-0">© 2024 Trace</div>
			<div class="flex gap-8">
				<a href="#" class="hover:underline">Terms of Service</a>
				<a href="#" class="hover:underline">Privacy Policy</a>
			</div>
		</div>
        
        <div class="flex justify-center mt-12 mb-4">
            <div class="flex flex-col items-center gap-2">
                <div class="text-[10px] uppercase tracking-widest text-center max-w-xs leading-relaxed">
                    All Your Angles. Every game, every player, every moment.<br>
                    Available in U.S. and Canada
                </div>
                <div class="mt-6">
                    <div class="w-8 h-8 bg-black text-neon-yellow rounded-full flex items-center justify-center">
                        <Plus size={20} />
                    </div>
                </div>
            </div>
        </div>
	</div>
</footer>

<style>
	/* Custom animations or utilities if needed */
	.animate-spin-slow {
		animation: spin 10s linear infinite;
	}
	@keyframes spin {
		from { transform: rotate(0deg); }
		to { transform: rotate(360deg); }
	}
</style>

