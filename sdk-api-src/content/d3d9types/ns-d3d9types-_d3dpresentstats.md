---
UID: NS:d3d9types._D3DPRESENTSTATS
title: "_D3DPRESENTSTATS"
author: windows-driver-content
description: Describes swapchain statistics relating to PresentEx calls.
old-location: direct3d9\d3dpresentstats.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dpresentstats.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DPRESENTSTATS, D3DPRESENTSTATS structure [Direct3D 9], _D3DPRESENTSTATS, d3d9types/D3DPRESENTSTATS, direct3d9.d3dpresentstats, f8128846-be10-11db-bbc4-ca2a39414774
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DPRESENTSTATS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DPRESENTSTATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DPRESENTSTATS structure


## -description


Describes swapchain statistics relating to <a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">PresentEx</a> calls.


## -struct-fields




### -field PresentCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Running count of successful Present calls made by a display device that is currently outputting to screen.  
          This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.
          


### -field PresentRefreshCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.


### -field SyncRefreshCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter. 


### -field SyncQPCTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

The scheduler's last sampled machine time, obtained by calling 
          <a href="https://msdn.microsoft.com/08169390-940b-4110-813a-249d107cc953">QueryPerformanceCounter</a>.


### -field SyncGPUTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

This value is not used.


## -remarks



When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics 
        at any point in time.  In effect, they can do the following.

<ol>
<li>Render to the back buffer</li>
<li>Call Present</li>
<li>Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</li>
<li>Render the next frame to the back buffer</li>
<li>Call Present</li>
<li>Repeat steps 4 and 5 one or more times</li>
<li>Call GetPresentStats and store the resulting D3DPRESENTSTATS structure </li>
<li>Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures. 
          The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of 
          PresentRefreshCount increment and PresentCount assignment of frame presents.  If the PresentRefreshCount last sampled does not 
          match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)  </li>
</ol>
Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and 
        GetPresentStats (by calling GetPresentStats API at any two points in time). For example, a media application that is presenting at the same rate 
        as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present 
        frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.

The application code looks like the following sequence.

<ol>
<li>Render frame A to the back buffer</li>
<li>Call Present, PresentCount = 1</li>
<li>Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</li>
<li>Render the next 4 frames, B, C, D, E, respectively</li>
<li>Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</li>
<li>Call GetPresentStats and store the resulting D3DPRESENTSTATS structure </li>
<li>Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.  
          If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, 
          then the last presented frame should be frame C.  Because the application presents once very vblank interval (the refresh rate of the monitor), 
          the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks. </li>
<li>	Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.  
          If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), 
          then no frames have been dropped.  If the second PresentCount is 3, which corresponds to frame D, 
          then the application knows that one frame has been dropped.</li>
</ol>
Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx 
        calls.

<b>Windows Vista:  </b>The Present calls will be queued and then processed before GetPresentStats 
        call will be processed.

When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to 
        re-synchronize with the vblank.  To do this, an application can simply not render the late frames and start rendering with the next correct frame 
        in the queue.  However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called
        D3DPRESENT_FORCEIMMEDIATE.  The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame 
        will be processed immediately within the next vblank interval, effectively not visible on screen at all.  Here is the application usage example 
        after the last step in the previous example.

<ol>
<li>Render the next frame to the back buffer</li>
<li>Discover from PresentRefreshCount that the next frame is already late</li>
<li>Set Present interval to D3DPRESENT_FORCEIMMEDIATE</li>
<li>Call Present on the next frame</li>
</ol>
Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics 
        does not change in that scenario.

D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications. 

<b>Windows Vista:  </b>Use the DWM APIs for retrieving present statistics.

When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of 
            limited accuracy.

<b>Windows Vista:  </b>If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, 
        then it can experience a graphics glitch. A glitch is a so-called visual hiccup. If a monitor is set to refresh at 60 Hz, and the application 
        can only manage 30 fps, then half of the frames will have glitches.

Applications can detect a glitch by keeping track of SynchRefreshCount. For example, an application might perform the following sequence of actions.

<ol>
<li>Render to the back buffer.</li>
<li>Call Present. </li>
<li>Call GetPresentStats and store the resulting D3DPRESENTSTATS structure. </li>
<li>Render the next frame to the back buffer. </li>
<li>Call Present. </li>
<li>Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</li>
<li>Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures. 
          If the difference is greater than one, then a frame was skipped. </li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

