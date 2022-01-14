# How The Internet Works

## A Primer for Everyone

[Jason Norwood-Young](mailto:jason@10layer.com)

The amount of time between you entering a web address and a web page opening in your browser is staggeringly fast – usually measured in milliseconds. This belies the incredibly complex process between you hitting "enter" and words, pictures, video and sound appearing on your computer from potentially the other side of the planet earth. In between those two events are a myriad of incredible moving parts that somehow work reliably in-sync, very close to the speed of light, to make the magic happen. 

Most people don't know, or think about, exactly how it works. And I don't mean just most laypeople – most computer people don't give it much thought either. Exceedingly few will know all the bits and bobs that make the whole thing work. It's so complex that it's difficult to hold in your head at once, and as long as it's all working, it's unnecessary to be too concerned about it all anyway. A mechanic doesn't consider the chemical reaction that takes place when you combine ancient rotted vegetable mass, oxygen, and electricity, every time they turn the ignition on a car. I certainly don't – I'm just happy that it goes "vroom" and takes me from one place to another. That doesn't make the process of driving an exploding mass of steel and fossils any less incredible.

So what, exactly, does happen from the moment you enter a web address, (or, in geek-parlance, a universal resource locator, or URL) into your browser and hit enter? It's a lot, kids. A whole hell of a lot.


# Your place on the web

The web address, or URL, has become so recognisable as part of our culture that we seldom stop to think about how weird it is. Why do we have different endings, like .com, .org, or .co.za? Why do we sometimes have www at the beginning, and sometimes we don't? Sometimes I see "http://" and sometimes "https://", but I don't even need to include them in the URL. Why? Who looks after all this stuff, anyway? Who invented it? And what's with all the dots?

To answer the last question first, here's a little secret about computer engineering: many decisions are made completely arbitrarily, then everyone starts doing it that way, and we can never, ever, ever go back. And that's the story with the dots, invented by the chap who is considered the father of the web, Tim Berners-Lee. The dots, Berners-Lee admits, [were a mistake](https://www.thetimes.co.uk/article/backslash-web-creator-sir-tim-berners-lee-apologises-for-his-strokes-srrzjsjtssp) – he wishes he'd used forward-slashes throughout the URL. He also regrets the two forward-slashes after the "http:", where one would have sufficed. An arbitrary decision that has become a ubiquitous part of modern culture. 

Whether we use dots or forward-slashes (and I am quite partial to the dots, mistake or not), they represent different stages of an address. That address will eventually tell us exactly where a server lives that stores the web page that we're looking for, but first we have to ask for directions to that server. Each part of the URL, starting from the end, tells us where to ask for the next part of the directions. 

If we think of it as an address – [Santa Claus, 123 Elf Road, St Nickville, North Pole](https://www.usatoday.com/story/news/nation/2019/11/18/operation-santa-delivers-exact-street-address/2555659001/) – it works in much the same way. We start at the end, which tells us the country. Then we move to an area (I've made up St Nickville, the official Santa address just has a road name, which makes me suspicious that it's just made up), and finally we start to hone in on a street, house number and recipient. 

What we call "top-level domains", the last portion before the dot, is often a country, just like a regular address. Just about each country gets its own, such as .uk for the United Kingdom, .za for South Africa, and .cn for China. (They are based [on a list](https://www.iso.org/iso-3166-country-codes.html) maintained by the International Organisation for Standardisation, or ISO, and created by the United Nations.) 

The notable exception for this rule is the United States. While the web, and internet as a whole, are designed as being country-agnostic, there's no doubt that the US has nominated itself as the Benevolent Dictator For Life, and sees itself as the custodian, if not the owner, of the internet. (The internet, and computing in general, is full of these "benevolent dictators". Just how benevolent they are is open to broad interpretation, personal opinion, and sometimes just plain marketing.) While anyone can purchase a .com or .org domain, there is some assumption that the site is likely to be American. Some top-level domains, such as .mil for military and .gov for government, are very distinctly reserved for the US. The .us is implied. 

This tacit control of the internet does raise legitimate concern for other countries, especially those not politically or socially aligned with the US, which has unfortunately led to some fragmentation of the internet. North Korea runs its own version completely, while China blocks much of the Western internet from its population. 

Fortunately, a slew of non-country-specific top-level domains have become available over the last few years, including .biz, .info, .museum, and one absolutely good reason to clear your browser history, .xxx, specifically for adult content. 

There really [are a lot of top-level domains available nowadays](https://en.wikipedia.org/wiki/List_of_Internet_top-level_domains), which has gone a long way in relieving the pressure on .com, which was prone to cybersquatting, the practice of registering domains simply to sell them on to the legitimate owners. These parasites of the internet turned a healthy profit in the early days by registering coveted (and often branded) domains for the sole purpose of sitting on them until someone paid their asking price, before resolution policies by the registrars, some high-profile court cases and the new top-level domains leveled the playing field. (The Internet Corporation for Assigned Names and Numbers, or [ICANN](https://www.icann.org/), is the organisation that decides on new top-level domains.) 

When you "buy" a domain name, whether for cybersquatting or legitimate reasons, you go to a domain merchant, known as a registrar. These registrars are appointed by ICANN, and can then sell you a domain name, usually for a limited period of time. Different registrars control different TLDs, so there is a bewildering number of prices and terms for domains. Third-party registrars resell on behalf of the primary registrar, which means it often pays to shop around. When you register the domain, information such as your name, address and telephone number are listed, publicly, with the domain. However, many of the registrars will nowadays offer to protect that information (usually for a fee). It's worthwhile doing even if you have nothing to hide, just to avoid the spams and scams that you'll get as soon as your email is attached to the domain name. 

If you don't already own your own domain name, I encourage you to go through the process of purchasing one. The domain name you choose to buy, provided it's available, is limited only by your imagination. Once you have it, you can use it for your email address, a website, or simply to own your own address as of the global internet amongst the [365 million other registered domains](https://www.verisign.com/en_US/domain-names/dnib/index.xhtml). 


# Where would you like to go today?

Translating one of those 365 million domains to an actual server's location in less than a blink of an eye uses a technology called DNS, or the Domain Name System. Along with your name, telephone number and address that gets registered with the registrar, another field, the DNS server address, is also stored. (Technically, a number of DNS server addresses are usually stored, typically four, for redundancy. But for simplicity we'll pretend this is a single server.) This address, represented by a bunch of numbers called an IP address, which we'll get to in a minute, in turn has a list of domain names associated to other IP addresses. This allows you to have multiple subdomains, such as "[www.example.com](www.example.com)", "email.example.com", or simply "example.com". (The domain "example.com" is interesting in itself, being a reserved domain on the internet for people like me to use in examples without pointing at a real site.) 

So when you hit "enter" on your web browser, your browser will first find the correct registrar to look up the domain name, then it will receive the DNS address, and then it will query the DNS to get the IP address of whatever it's looking for. So far your browser has had two full conversations, and it hasn't even started downloading the site. All it has is a set of numbers, that looks something like 93.184.216.34 (the IP address of example.com). This address will tell it how to get to the server that hosts the website we're looking for. We're just getting started.


# Pushing the boundaries of conservatism

The whole process seems a little convoluted. And trust me, we're just getting started on the convolution. It almost seems like it's a process designed by a committee. How can the internet, the love-child of marxism and the hippy movement, be so clunky and bureaucratic? It comes back to the founding principles of the internet, a glorious mix of liberal idealism and conservative standardisation.

I quote [its principles](https://webfoundation.org/about/vision/history-of-the-web/) directly from the World Wide Web Foundation, run by Berners-Lee himself:



* Decentralisation: No permission is needed from a central authority to post anything on the web, there is no central controlling node, and so no single point of failure … and no “kill switch”! This also implies freedom from indiscriminate censorship and surveillance.
* Non-discrimination: If I pay to connect to the internet with a certain quality of service, and you pay to connect with that or a greater quality of service, then we can both communicate at the same level. This principle of equity is also known as Net Neutrality.
* Bottom-up design: Instead of code being written and controlled by a small group of experts, it was developed in full view of everyone, encouraging maximum participation and experimentation.
* Universality: For anyone to be able to publish anything on the web, all the computers involved have to speak the same languages to each other, no matter what different hardware people are using; where they live; or what cultural and political beliefs they have. In this way, the web breaks down silos while still allowing diversity to flourish.
* Consensus: For universal standards to work, everyone had to agree to use them. Tim and others achieved this consensus by giving everyone a say in creating the standards, through a transparent, participatory process at W3C.

The mix of decentralisation and design by consensus are two of the key ingredients of the web's success. Without the consensus, it would be inoperable chaos. Without decentralisation, it would never be widely adopted. Add to this that Berners-Lee decided to perpetually let the world use his technology for free, without any restrictions, and you have the seed for what has grown into the giant, world-spanning tree of the internet we see today.

But design by committee can be frustrating, especially for us techies that have an unhealthy obsession with new and shiny technology. Regularly, an individual or organisation will release a new technology and proclaim it a "standard". One of two things happen in this case – it hobbles along for a while until it fades into obscurity, or it gets its own committee that starts developing it via consensus, and it has the same problems – slow to change, baked-in mistakes that can never be corrected – as all the other web technologies. Javascript is a great example, developed initially in a great rush of creativity to bring some interactivity to the web, and nowadays moving glacially slowly in adopting new features that everyone can agree on. This stability however is what allows the greater Javascript community to thrive. By having a stable platform to develop on, software developers can safely invest in training and development, and build a much larger, and more dynamic environment than the solid but somewhat stagnant base that it's built on. 

The Worldwide Web Consortium, better known by its catchy acronym W3C, is in charge of setting standards for the web, and you can imagine the difficulty in getting the 458 members to agree to any change in standard. Any change that breaks historic websites, some of which are over 30 years old, is unacceptable. For a new feature to have any meaning, it needs to be implemented on every web browser. Since many web users don't upgrade their browsers very often, websites implementing the latest, greatest features need to be able to display a downgraded experience for users running browsers that don't support a specific feature. 

Another example of the slow pace of change has been the adoption of IPv6, which was designed and drafted by the Internet Engineering Task Force (IETF) in 1998, but took until 2017 to be adopted, and we are only starting to see it in use today. 


# IP Freely

Hold up, IP what? An IP, or internet protocol, address, as mentioned before, is a bunch of numbers (four, to be precise) separated by dots. Everything on the internet gets an IP address. The server your are getting content from has one, which is why we go through that whole process of changing a domain name (example.com) into an IP address (93.184.216.34). Each of the four numbers range from 0 to 255. (255 is a popular number in computing, since computers like to count in binary – zeros and ones – and eight consecutive ones (11111111) in binary equals 255 in our decimal notation). 

When I say everything gets an IP address, I do mean everything. Your computer, your cellphone, your TV, your security system, and increasingly the "internet of things" like your toaster and fridge and lightbulbs and car, all get IP addresses. In a large factory, every sensor on every machine gets an IP address. Back in 1998, it was already clear that while the number 255.255.255.255 gives us a lot of potential combinations, about 4.3 billion to be precise, we would eventually run out. (There's some addresses that are reserved for non-internet purposes, such as 127.0.0.1, which points back at the device, also known as the "home address". Next time you see a t-shirt that says "There's no place like 127.0.0.1", you'll know what it means.) 

The four-part IP address is known as IP version 4, or IPv4. Version 6 of the IP address system, which took from 1998 to 2017 to be ratified, uses eight groups of numbers, so double that of IPv4. It also uses hexadecimal to count, a number system that goes from zero to 15. (To count in hexadecimal, once you hit 9, you use A for 10, B for 11, C for 12 etcetera until F, which equals 15. Where in binary you need eight ones to represent 255, in hexadecimal, 255 is written as "FF".) The combination of four hex characters eight times gives us an astonishing 340,282,366,920,938,463,463,374,607,431,768,211,456 possible addresses to use. (340 trillion, trillion, trillion.) It is safe to say that we will never run out of IP addresses. Every atom on planet earth can get 100 IP addresses before we run out. An IPv6 address looks something like "​​2001:db8::8a2e:370:7334" – for brevity we skip out the extraneous zeros which is why some of the groups are shorter than four characters, and some are completely empty. 


# Passing down the line

Now we know the IP address of the server we would like to get information from, it's time to figure out how to get there. The first thing your browser will do will be to wrap your information into a nice little parcel, called a "payload", and put a label with the delivery address, return address, and some more info on it, called the "header". The header and payload together are called a "packet", just like the cookie package you might get from your Gran. (In some cases they do in fact contain digital cookies.)

These packets are how all data is sent to and fro on the internet. A packet can only be a maximum size, so when something exceeds that size, we end up sending multiple packets. If you imagine a little bike courier office with lots of couriers, those couriers grab the packets as they come in and zip our on their bikes. However, they don't always take the same route. Sometimes a packet you send first arrives later than one you've sent second. Sometimes the couriers get run over by a truck and your packet never arrives. (You may have heard the term "dropped packets".) Sometimes it does arrive, but the courier has opened, found the cookies, had a few, and then tried to seal it back up in the hopes you won't notice. Bike delivery is clearly not to be trusted.

Adding to the confusion, the bike drivers don't really have GPS, either. They have some kind of idea of how to get to the first part of the address, the first set of numbers in the IP address, but once they get there they have to ask for directions. Sometimes they get passed to the the next part of the address, but sometimes they just get sent to someone else who might know. This is called "routing", with the packets routed from one router to another, anywhere on the internet. The whole internet tries to keep a record of which routes are closest and best, so once one router establishes a good route, it tends to recommend it most of the time. 

Given the chaos and anarchy, it's surprising the internet works at all, let alone as well as it does. From the madness, patterns emerge. Shortest and fastest routes are established. Dropped packets are resent. Corrupted packets with some of the cookies eaten are discarded (using "parity" – a way to check if we have missing cookies) and a letter is sent to your Gran requesting more. If a packet arrives out-of-order, we just wait patiently for the slower bike messenger. 

Within the payload of these IP packets, we will often have a very similar-looking packet – a box in a box, if you will. It will also have its own header and payload, but it's not an internet protocol packet, it's an HTTP packet. And this brings up a very important point…


# The web is not the internet

While we might think of the World Wide Web, with its Facebook and Google and Wikipedia and your weird friend's old-fashioned blog as all being "the internet", it is merely a small passenger on a very large jumbo jet, catching a lift. The internet is the thing that transports data from place to place, but you can run all kinds of crazy services on it. WhatsApp, for instance, uses the internet, but not the web, to send messages between you and your racist suburb group. When we talk about IP phones or IP TVs, we're using the internet, but not the web, to transmit voice or video. Email is another biggie, using the internet but not touching the web, unless you're using the web to view the email using something like GMail once you've received it. The web has become a very, very big service using the internet to do what it does, but the internet doesn't care. It has toasters to update, large factories to monitor, spam to deliver, and Tesla drivers to A/B test on. 

Internet (and networking) people love to talk about "layers". It's "layer one" this and "layer four" that. To demystify this, "layer one" is the actual physical network, like a wire between one router and another, or a wifi wave, or a satellite link to space and back. Layer four is the application layer, where the web lives. (Or to give it its correct name, the HTTP layer.) All the IP stuff sits in layer two, while layer three deals with TCP, or Transfer Control Protocol, another protocol that handles the safe delivery of our packets – essentially ensuring our bike messengers get where they're going. (IP and TCP are usually lumped together, known as TCP/IP.) 


# Get this. Put that.

Back to the HTTP packets, the thing that makes the web the web. And you can see an HTTP packet in action, if you just open the "Developer" console on your browser, go to the "Networking" tab, and refresh. You'll probably see quite a lot of action, as your browser hits multiple resources to serve up the smorgasbord that is a modern website. Looking at any single request will show you the "Request Headers", and the "Response Headers". The Request is what your browser has sent to a web server. 

Usually we don't include a payload on that initial request, because we are just requesting a simple webpage and don't need to send any data along with it. The important fields are the method, the path, and the schema. 

On most requests, the method will be "GET", which, obviously, says I would like to simply get some information back. Another common method is "POST", which tells the site that I'm sending it some data in the payload. When you fill in any form and hit "submit" on the internet, it'll do a "POST" with the data you've submitted in the payload section of the package. 

Since at first we're just putting a URL in our browser, the first thing will be the GET. If there is anything after the URL, such as [www.example.com/test](www.example.com/test), the path field will show the "/test" portion of the URL. It's not important for our DNS lookup or our routing, but it could be important to the server we're sending it to, so it's included in the GET request header.


# Security! Security!

Then there's the schema, usually "http" or "https". This is the first part of the URL, and something we haven't explored just yet. As we've seen, http stands for "hypertext transfer protocol", but if we add the "s" we mean it needs to be "secure". Honestly, if you'd known how insecure http alone was, you'd have never used the damned thing. While more and more sites are https-only, there are still plenty of sites using http only. And when you use insecure http, your ISP, their ISP, and anyone on the same network as you has almost unlimited access to the data you send. Until a few years ago, it was trivial for hackers to connect to public wifi, grab the cookie (this time, a digital cookie) for your Facebook connection, and then masquerade as you on your account. (Or your bank, for that matter.) If you happened to enter a username or password while you were online, it was grabbed and recorded. The hackers didn't even have to work hard at it – simple web browser extensions would do the hard lifting for them, scanning the wifi for the words "username" and "password" when you submitted any form, to make password hacking quick and easy.

One of the reasons adding that "s" to your website was so unpopular until recently is because it cost a heck of a lot of money. It was worth it for a bank or a large social media company, but if you're an individual running a cooking recipe blog, you probably weren't going to shell out for an SSL (Secure Socket Layer) or the more modern TLS (Transport Layer Security) certificate. 

The thing that made it so expensive was that you needed to get the certificate authorised by a third party, and only a few of these third party organisations were trusted enough to issue these certificates. But for the past few years, since 2015, an organisation called [Let's Encrypt](https://letsencrypt.org/), a non-profit working to make the web safer, has offered free SSL/TLS certificates to anyone who wants them. (260 million sites are protected by Let's Encrypt at time of writing.) 

Along with the third-party stamp of approval that comes with a certificate, all traffic between you and a website is encrypted with SSL/TLS. (Apart from which website you're visiting… be careful with those ".xxx" domains, your ISP, as well as the CIA, know exactly what you're looking at.) Any passwords, usernames, or cookies that pass between you are secure, so your session can't be hijacked, your password can't be stolen, and hackers, ISPs and governments won't know which paths you're visiting on a specific website.

Not that you're guaranteed security just because there's one of those locks in your browser address bar, an indication that you've connected to an HTTPS server. Hackers are clever and resourceful, and can still attack your computer, compromise the server, or if they're motivated, perform a "man-in-the-middle" attack where they hijack the certificate itself. There's also a concern that the emergence of quantum computing will see all our encryption crumble before the sheer computing power we expect in the future. 


# Loading…

We've sent our GET packet, it's taken a lift on an IP network, and finally we get a response, also in an HTTP packet wrapped in an IP packet, and also with a header, and hopefully that header contains the field "content-type", with the value "text/html". Peeling open our boxes, inside we find our payload… beautiful, structured HTML. Lots of angled brackets and forward-slashes, weird esoteric instructions, and buried in it all, the actual content of a web page that our browser throws onto our screen in all its glory. 

Hypertext Markup Language (HTML) has come a hell of a long way, and not everyone agrees that the path it's taken was a good one. The original intent was for a bit of formatting (the Markup), links within and externally (Hypertext), all wrapped up in a reasonable-to-read common language. The monsters we see today, with interactivity, animation, styling, automatically redesigning the layout based on screen size for mobile phones (what we call "adaptive" and "responsive design")... it's all a bit much really. 

Sidebar: 


## The Javascript problem

The New York Times loads about 180 separate files, containing 16MB of data, for its front page. The King James bible, both old and new testaments, is about 4.13MB big, so the New York Times front page is over 3.8 times as large. Yet I could read the entire front page of the NYT in a few minutes, so where the heck is all this data coming from?

An image is worth a thousand words, and when we're talking about web pages, we mean that very literally. Images account for about 2.1MB of data, or half a bible. Video is much heavier than an image, and even though there are only a few, they account for 3.6MB. (They're mostly adverts that load in their own time, not stopping you from using the page while they load, so we can just about ignore them.) Plain HTML – especially the primary page for the New York Times, takes up a surprising amount, 1.5MB. Stylesheets account for only 240KB, and fonts 268KB. But the real culprit on the New York Times, as well as so many other pages, is Javascript. It's 2.8MB, which, when one considers it's just plain text, is an enormous amount. Over a bible of code for interactivity on a web page that is largely static. 

We tend to see the web as a costless method of communication, but this is not true. All those packets moving across the wire are driven by electricity. The New York Times' front page contains only 22,015 characters, so in terms of text, it should be 22KB, plus some HTML formatting, say another 100KB to be generous. Add the images, the fonts and styling, we're still not at a full bible. Between the Javascript and the video, we hit astronomic amounts of data, served every time someone visits the New York Times for the first time. With [327 million visits in the last six months](https://www.similarweb.com/website/nytimes.com/#overview), that's 873 terabytes of data delivered in Javascript alone. Multiply this over all the sites on the internet, the largest of which tend to have similar Javascript bloat problems, and the cost becomes enormous.

End Sidebar

Despite concerns as to the sheer volume of data we're moving down the pipe, chopped up into IP packets, something miraculous happens when it reaches our computer. (Or phone. Or internet-enabled fridge.) A web page appears, formatted fairly consistently across devices, browsers, and operating systems. If you were a web developer during the early internet years, you'd understand what a miracle this is, what a long way we've come. Sticking to standards, especially when they're designed by a committee moving at a glacial pace while developers wanted to surge forward, was difficult at first. Vendors also wanted to gain a competitive advantage by offering features before their competition, even if those features had never seen a draft paper. New stuff is undoubtedly cool, and we owe a lot to those early browser pioneers, some of their crazy ideas did drive the direction of the web. But if you'd lived through those years, you'd appreciate the slow, steady pace of the W3C today, as well as for how blessedly the browser vendors stick close to the specifications when once they were on their own missions. Safari, Opera, Chrome, Firefox, Edge… whatever I use, I'm guaranteed a pretty good experience. (Provided, of course, the web developers also adhere to the same standards.) 

That's the one miracle. The other is that the entire process of fetching a web page, from domain name lookups to routing, to the to-ing and fro-ing of packet delivery across a shared, malleable infrastructure, happens in milliseconds. And one more miracle: the internet remains, after all these years, free. All the organisations and committees I've mentioned, and a whole lot more like the Electronic Frontier Foundation (EFF), the Internet Assigned Numbers Authority (IANA), the Institute of Electrical and Electronics Engineers (IEEE), and the Internet Technical Committee (ITC), work tirelessly, usually thanklessly, and based on donor funding and volunteer work, to keep the magical internet beast alive and growing. 

So many have given so much, for free, to the internet, like Berners-Lee, Linus Torvalds, Jimmy Wales and Aaron Schwartz. That's why I'd like to licence this article with the Creative Commons license, developed by Lawrence Lessig, also free for use. 

This book is licensed [Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/). You are free to share it by copying and redistributing the material in any medium or format. You can also adapt the book by remixing, transforming, and building upon the material for any purpose, even commercially. This license is acceptable for Free Cultural Works. I cannot revoke these freedoms as long as you follow the license terms. However, if you share or transform it, you must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests I endorse you or your use of my work. If you remix, transform, or build upon the material, you must distribute your contributions under this license. For portions of the book that are already in the public domain, or if your use falls under the definition of fair use, you don't have to comply with the license. You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits. I also give no warranty for this work. If you injure yourself or others with this book, or if I've hurt your feelings or broken your brain, don't come crying to me. Also be aware that tThe license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material. If you want to get the full details of the license, [read the legal code here](https://creativecommons.org/licenses/by-sa/4.0/legalcode).
