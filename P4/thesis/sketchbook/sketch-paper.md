# 0. Title: 
Geofront: A Browser-based geoprocessing platform for the era of cloud-native geodata.


# Introduction

## Context
```
- Web GIS 

- Cloud native movement

- Thick client movement



[JF]: Which term to use? 
- Web GIS
- Web application
- browser-based application
- web tool
- GIS tool
```
Interactive web \ac{giss} form an indispensable component of the modern geospatial software landscape. 
For the average person, a web application is often their first and only exposure to a \acs{gis}, be it a web mapping service, a navigation system, or a pandemic outbreak dashboard. 
A web application is cross-platform by nature, and offers ease of accessibility, since no installment or app-store interaction is required to run or update the app: 
As soon as it can be found, it can be used.
The ability to share a full application with a link, or to embed it within the larger context of a webpage is also not trivial. 
Together, these aspects have made the browser a popular host for many important geographical applications, especially when accessibility is vital.
<!-- THIS ALSO MAKES IT EXTREMELY IMPORTANT TO DEVELOP WEB TOOLS -->
<!-- %  Tools like Leaflet and Celcium are widely used. -->

A significant development within the Open Geospatial Consortium (OGC) is the recent attention around "Cloud Native geospatial". This movement envisions a future of geodata as large, singular, statically hosted files, accompanied with cloud-based geoprocessing tools similar to the Google Earth Engine. This architecture would 
- make use of near-infinite resources in the shape of supercomputers and cloud-storage.
- finding large-scale patterns 
- This will be easier and cheaper for data providers, 
- and allows for cloud-hosted geodata to be more easily be consumed by cloud-compute tools. 
- This really is a 'new era'
The cloud-native initiative aims to radically simplify geodata storehouses to just static file servers. All processing and analysis of this geodata can then be performed by separate cloud-based web services.

For web GIS, this would offer direct data streaming options.  
```
- Data streaming 
- Other Trend: Gaming PC streaming: https://shadow.tech/en-gb/
```

At the same time, a trend within web applications in general shows an ever growing preference for so called 'fat clients' and 'thin servers', as opposed to 'thin clients' and 'fat servers' \cite{panidi_hybrid_2015}. This means that certain responsibilities, such as navigation, increasingly are being performed by the client rather than the server. As a consequence, applications are more quick to react on a user's input, and web-applications 

Geo-computation as a phrase is used to group all the various ways geodata is transformed, such as reprojection, translating between datatypes, or boolean operations. 


The trend can be attributed to new browser features such as WebAssembly, and performance upgrades of the javascript runtime (V8, JIT compiler, etc.).
```
... Blurring the lines between browser-based application, and desktop / native application.
```

<!-- This movement contains aspects of the ungoing trend of 'thin server' 'thick client'. -->

This trend is visible within web GIS 
towards more complex clients and simpler servers .
Within the field of geo-informatics, the move towards client-side heavy applications also caused academic and commercial interest for the prospect of \emph{client-side geoprocessing}.  -->
Whereas before the client was mainly use to visualize end results (leaflet, Celsium), now applications arise allowing users to edit (ninja) and validate (cjval) geodata, directly from within the browser. 
EXTREME EXAMPLES: GEOTIFF.

```latex
% A clear trend within these geo-web applications, is a push for increasingly complex applications. 
%   - Such as the ninja cityjson web viewer
%     - Proofs that the web can not only be used as viewer or end-user application, 
%       but also for geodata analysis and editing.
%     - Geocomputation
%     - Both for end-user tools, and tools used by developers.
%   - Also, Modern web tools such as webassembly allow us to run native geo-analysis applications directly in a web browser
%     - Leading to tools such as cj-val, a 3D city validator.

% TREND : HEAVY CLIENT-SIDE FOR INTERACTIVITY 
% client-side heavy web applications  

% One of the biggest benefits of this setup is \emph{Interactivity}. 
% If logic runs in the client, it can more quickly react to behavior of the user. 
% A full client-server roundtrip containing lots of geodata will in many situations take longer.


------------------------------------------------------------------------------- 


```

## Problem: 

```
RAISE QUESTIONS:

- Opportunities 
  - Name the positive changes
- Challenges: 
  - What is the role of web GIS in this new era? 
  - Where to facilitate geoprocessing functionalties? 
  - Will be go back to server-heavy architectures? 
  - Will be add responsibilities 



- 
```

When viewing the trend of Cloud Native Geospatial together with the advancements of web clients, a pattern emerges: 
Major opportunities are coming to the field of Web GIS tooling. Increasingly powerful options for server-side and client-side computation are, or will be, available for developers. More data & more services are becoming more open, and the lines between cloud-based, desktop and browser-based applications are getting increasingly blurry.

These developments lead to a critical re-examination of the **architecture** and **role** of web GIS applications, and this is particularly apparent for geo-computation. 

Regarding **architecture**, when OGC web-services are substituted by statically hosted, singular geodata files, all of their current geo-computation functionalities will have to be provided elsewhere. 
These can either be facilitated by other, new web-services, or can be added to the responsibilities of (web) clients.
The same dichotomy can be found in web-GIS applications wishing to use general geoprocessing capabilities. Developers of these applications will have to choose between hosting / paying for cloud-based geoprocessing services, or adding these often heavy computations to client applications.
This choice is also not a binary one. Hybrid approaches have proven to be beneficial \cite{csg_2016}, And as such, it is very likely that both architectures could operate in a complimentary manner. 

```
This is why we see that as soon as geodata is sufficiently findable, accessible, interoperable, and reusable, the accessibility concerns of geodata start to move more towards geodata _processing_ and _processing applications_.


```

Regarding **role**, the more accessible geodata becomes, the more accessible the _means to use_ geodata must become in order to keep up. After all, FAIR geodata means little if the means to access, compute, or visualize geodata are not accessible. 
Chris Holmes already envisions how cloud native will lead to expand the geodata community, and expand geodata users. "(cloud-native geospatial) is what gets geospatial out of its niche" \cite{podcast}.
We also see this happening with certain web applications like GeoTiff & ModelLab.
Modellab in particular states that _"Widespread access to frequent, high-resolution Earth observation imagery has created the need for innovative tools [...] that will help individuals and organizations to effectively access, analyze, edit, and visualize remotely sensed data in transformative new ways without years of specialized training or ongoing investments in proprietary software and technology infrastructure."_. \cite{modellab}

```
...
```
The previously named accessibility advantages give web GIS a lead compared to desktop applications in this pursuit of "denichifying" geo-computation.


```
THE CHOICE 
With both the possibility of cloud-native geoprocessing servers, and powerful clients,   
1. In any case, complex decisions, we need more data. 
It becomes clear that developers of web GIS applications will have to make important decisions.
in any case, more info, more experimentation, and thorough investigation on both server-side and client-side geo-computation is required. 
this study seeks to investigate the possibility, 
implementation and ramifications of the second option.
While both options are entirely possible, 
```
the choice, disregarding synergy.

The case for cloud-based geo-computation: very fast, 'infinite resources', google earth engine.

The case for client-side geo-computation: less clear. sees less research, less interest.  

with the general movement moving to the cloud, it becomes even more important to look at alternatives. 
- If study fails: we know that the move to the cloud is a wise one
- If study succeeds: we learn that in certain scenarios, client-based geo-computation is advantageous, and not ALL geo-computation should be done in the cloud.

this is why we study the second option.

This option matches the aforementioned trend of 'thin servers & fat clients', 
and the purpose of the Cloud Native movement to relieve data providers from the burden of setting up and maintaining multiple web services. 
It is also cheaper to perform client-side geoprocessing on the machines of end-users, 
instead of maintaining or otherwise paying for additional geoprocessing web services. \STUDY FROM 2019. 
<!-- argue early data consumption promotes interactivity -->
Finally, the prospect of Cloud Native geodata, combined with powerful geoprocessing additions to accessible web clients, 
opens up interesting new functionalities and use-cases for browser-based GIS. \STUDY FROM 2019

The challenges of this second option are that browser-based geoprocessing (BBG) might not be as performant as server side geoprocessing, \STUDY FROM 2015, 2016
and that the browser-based ecosystem lacks powerful geoprocessing tools like CGAL and GDAL. Additionally, how to present the complex endeavour of geoprocessing in the format of an accessible web application is unknown, and which use-cases might benefit from BBG also remains to be seen. 


## This study

```
- Goal: 
  - Re-examining the role of web GIS in an future era of cloud computation
  - Helping the decision of choosing Cloud native geoprocessing and / or Client-side geoprocessing. 
  - 
  - Studying the technology landscape of the browser. 

 - Seeking new roles for the client in an era of cloud computation

```



This thesis explores adding geo-computation capabilities to a web browser. By not relying on additional web services, operational costs could be lowered for certain applications, making geodata processing more accessible \cite{scg-2019}. Additionally, doing calculations locally may unlock certain use-cases.

The challenges of this second option are that browser-based geoprocessing (BBG) might not be as performant as server side geoprocessing, STUDY FROM 2015, 2016
and that the browser-based ecosystem lacks powerful geoprocessing tools like CGAL and GDAL.

by conducting this study, this thesis hopes to gain insight in .... , and the role of the web client in the coming era of cloud-native geospatial data and computation.

The wider goal of this study is to discover the possibilities and limitations of browser-based geoprocessing, in order to help developers make the decision between browser-based geoprocessing and cloud-based geoprocessing. 
This is, however, too large of an undertaking for the scope of one thesis. Geoprocessing is a multifaceted phenomenon, containing for example map algebra, crs transformation, vector to raster translations, raster to vector translations, point cloud filtering and interpolation, just to name a few. 

Therefore, this study will develop a use case application to contextualize the research, and to force the research to solve the practical challenges of how \ac{bbg} can actually be used. The type of application chosen is a web-based geoprocessing environment, similar to GEOTIFF, GeoTrellis + ModelLab. These types of applications seek to present geoprocessing capabilities in an accessible manner.



<!-- donald knuth argument: by keeping geodata raw, and porsponing the consumtion of geospatial data to the last possible moment, we can  -->




## Use Case
This study introduces GeoFront, a web based, open source, geodata processing and visualization tool. 






<!-- find some altruistic good -->

These developments have far reaching consequences for web GIS as a whole. 


% POINT 1   
Firstly, this thesis anticipates that OGC Cloud native geospatial types, together with the trend of complex clients, will lead to a need for  



"Widespread access to frequent, high-resolution Earth observation imagery has created the need for innovative tools like ModelLab that will help individuals and organizations to effectively access, analyze, edit, and visualize remotely sensed data in transformative new ways without years of specialized training or ongoing investments in proprietary software and technology infrastructure. " 
% \cite{ModelLab}.


% Similar trends can be found with GEOTIFF.IO and MODELLAB 
A similar need arose when in the field of rasters, ...
leading to the development of tools like geotiff.io and modellab.

% Investigate what it means to create an accessible geoprocessing environment

The adoption of COPC could mean the same for point cloud data, but it remains unknown what accessible analyze, edit, and visualize means for point cloud processing. 
How to present the complex endeavour of point-cloud processing in the format of an accessible web application is unknown. 


% POINT 2



Academic sources 

\cite{kulawiak_analysis_2019, panidi_hybrid_2015, hamilton_client-side_2014}. 
Interactive geospatial data manipulation and online geospatial data processing techniques where described as "highly valuable trends in evolution of the Web mapping and Web GIS" (\cite{panidi_hybrid_2015}).


Commercial sources 




\section{This Study}

% CONTENT OF STUDY
This study introduces GeoFront, a web based, open source, geodata processing and visualization tool. 
It enables users to configure geodata processing pipelines using visual programming. 
Users are able to make use of native geoprocessing tools such as CGAL, visualize and debug both end results and in-between results.


% GOAL OF STUDY
Finally, this study intends to use the design, creation, and evaluation of geofront to gain insight into the broader topic of client-side geoprocessing. 
Geofront will be used as a proxy / experiment to assess: 
- The fitness of the web in general for client-side geoprocessing
- If client-side geoprocessing in its current state has any meaningful use-cases
- If new features of modern browsers mean anything for the field of geo-informatics at large (webassembly in particular). 




% Explain geofront
% The entire application runs client-side in a browser, and uses a visual programming language as its primary \ac{gui}.
% The main goal and feature of geofront is to take existing low level geoprocessing libraries, and to make these interactively usable on the web. 
% These libraries include a limited set of CGAL operations, complied from C++, and various geoprocessing algorithms such as Startin, written in Rust. 
% Being a visual programming language, GeoFront can be used to interactively alter the geodata pipeline. 
% In between products can quickly be inspected using a 3D viewer.

% PATH TOWARDS RESEARCH QUESTION
\todo{MAAK EEN DUIDELIJK LINK NAAR RESEARCH QUESTIONS \& ASSESSMENT CRITERIA}


% ## This thesis 


% This will be done by providing a web-based Demo Hosts to embed these demo's within. 

% ...

% By means of visual scripting, a user will be able to reconfigure the dataflow interactively, and 'toy' with the tools & data provided. 

% We will test how well contemporary web technologies support such an application, as well as judge aspects such as accessibility & performance of said application. We will also judge if this type of application is indeed beneficial and usable as a scripting / demo environment.  


% <!-- 
% These features could all be implemented by normal means ( buttons, panels, sliders ) -->

% CHOICE: do something in-between python bindings, and a full fletched end-user application. 
% Ergo: Visual programming




% For input, the environment offers \ac{wms} and \ac{wfs} support, as well as ways for users to load locally stored geodata. Parameters can be specified using various ui components, such as sliders. 
% For output, the environment can be used to either save data to the user's local machine, or to visualize the results within the geofront application using a WebGL based viewport.

% Accessibility
% - Shareability
% - Reproducibility

% Interactivity 
% - Visual programming 
% - Visual feedback & insight
% - Sliders

% # Some Introduction

% Web applications have many benefits over native applications
%   - cross-platform
%   - easy to distribute
%   - findable, accessible
%   - ...

% For these reasons the web has become a popular target for many applications, including geoweb applications. 
% - Tools like Leaflet and Celcium are widely used.

% A clear trend within these geo-web applications, is a push for increasingly complex applications. 
%   - Such as the ninja cityjson web viewer
%     - Proofs that the web can not only be used as viewer or end-user application, 
%       but also for geodata analysis and editing.
%     - Both for end-user tools, and tools used by developers.
%   - Also, Modern web tools such as webassembly allow us to run native geo-analysis applications directly in a web browser
%     - Leading to tools such as cj-val, a 3D city validator.

% This thesis seeks to push this trend further, 
% and explores to what end the capabilities of the contemorary web can facilitate the needs of geo-informatics in general, 
% and geodata processing in particular. 

% We introduce GeoFront, a web based, open source, geodata processing and visualization tool. 
% It enables users to configure geodata pipelines using visual programming. 
% Users are able to make use of native geoprocessing tools such as CGAL, visualize and debug both end results and in-between results.

% The input and output of the functions exposed by these libraries 

% the aspect of interactivity is 

% - The web gives us great \emph{Accessibility}, and making it client-side promises us great \emph{Interactivity}

% Browser based \ac{geoprocessing}, hereby known as \ac{bbg}, ... 


% 'interactive geo-processing'
% - Insight 
% - Reproducibility

% GOAL: - explore new use-cases of the web for interactive geo-processing.
    %   - explore the 'fitness' of the web for many different geoprocessing use cases. 

% 1. Build a general purpose web geoprocessing environment 

% 2. Study to which end different needs can be fulfilled / different use-case requirements can be met 

% Safesoft's FME, but web based & open source 




This study intends to discover if contemporary web technologies can facilitate a full-scale client-side geoprocessing tool, by seeking an answer to the following question: 




In recent years, a trend towards increasingly complex and demanding web applications is noticeable. 
-> not only end-users, editing, other examples of geoprocessing clients, etc...
browser-based geoprocessinG: GeoTIFF, GeoTrellis, ModelLab.

These web app increasingly rely on 'fat clients' and 'thin servers', instead of the traditional: 'fat server', 'thin client' paradigm. 
This trend can be attributed performance upgrades of the javascript runtime, and to new browser features such as WebAssembly. 




```




----------------------------------------






% Similar trends can be found with GEOTIFF.IO and MODELLAB 
% Investigate what it means to create an accessible geoprocessing environment




##
## This study
The goal of this study is to discover the possibilities and limitations of browser-based geoprocessing, in order to help developers make the decision between browser-based geoprocessing and cloud-based geoprocessing. 


This study investigates browser-based transformation of geodata, 
as well as how browser-based GISS might profit from from the new opportunities. 


## Use Case
The goal of "discovering the possibilities and limitations of browser-based geoprocessing" is too large of an undertaking for the scope of one thesis. Geoprocessing is a complex and multifaceted phenomenon, containing for example map algebra, crs transformation, vector to raster translations, raster to vector translations, point cloud filtering and interpolation, and much more. 

Therefore, this study will develop a use case application to assist this research. This application serves to contextualize the research, and to force the research to solve the practical challenges of how \ac{bbg} can actually be used. The type of application chosen is a web-based geoprocessing environment, similar to GEOTIFF, GeoTrellis + ModelLab. These types of applications seek to present geoprocessing capabilities in an accessible manner: "Widespread access to frequent, high-resolution Earth observation imagery has created the need for innovative tools like ModelLab that will help individuals and organizations to effectively access, analyze, edit, and visualize remotely sensed data in transformative new ways without years of specialized training or ongoing investments in proprietary software and technology infrastructure. " \Source{ModelLab}.

This study introduces GeoFront, a web based, open source, geodata processing and visualization tool. 
It enables users to configure geodata processing pipelines using visual programming. 
Users are able to make use of native geoprocessing tools such as CGAL, visualize and debug both end results and in-between results within a browser.
Instead of using cloud-based geoprocessing services, all calculations will be performed within the browser itself, in order to examine browser based geoprocessing.

Where ModelLab is build on top of recent improvements to the accessability of satellite imagery, GeoFront is build in anticipation to a similar development for point cloud datasets with the introduction of COPC. The focus of Geofront is therefore on point cloud processing, and point-cloud based modelling, such as Digital Terrain Models (DTM). 


## Research Question:
This study seeks to investigate browser-based transformation of geodata, 
as well as how browser-based GISS might profit from from the new opportunities.

"What are the advantages and disadvantages of browser-based geoprocessing within GeoFront?"

##  Sub Questions
- How to design and create an accessible browser-based geoprocessing client ready for cloud native geodata? (~Old Phase 2)
- How can browser-based geoprocessing leverage existing geoprocessing libraries? (~Old Phase 3)
- Is browser-based geoprocessing performant enough for this use case? (~Old Phase 1)
- Which use-cases might geofront serve? (Old Phase 4)

## 

<!------------------------------------------------------------------------------->
# Related work
```
...
```

<!------------------------------------------------------------------------------->
# Methodology:

... This study will conduct this investigation by developing a browser-based geoprocessing environment. 

## Web App
Geofront is designed as a client-side web application. On one level, the choice for native application or browser-based application is not very significant, as the line between these two types of applications continues to blur. Tools like Electron bring a 

However, 
 as opposed to a native application as an experiment on accessibility. 





## Use Cases 
Four use-cases are envisioned for browser-based geoprocessing in an era of cloud-native geospatial data and tools.

### 1 Educational
```
- Web Demo
```



### 2 Academic
```TODO
- Open Science
- Jupyter notebook
- Reproducibility 
```



### 3 End user app
```
- Exposiign 
- Retrieval, Processing, visualization in a browser app

```


### 4 Cloud Compute Prototyping
```
- Geoflow
- Sampling
- Trying different parameters
```


<!------------------------------------------------------------------------------->
# Implementation 

```
...
```
<!------------------------------------------------------------------------------->
# Discussion
```
...
```
<!------------------------------------------------------------------------------->
# Conclusion
```
...
```

