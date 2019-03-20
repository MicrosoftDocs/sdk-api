---
UID: NN:qnetwork.IAMExtendedSeeking
title: IAMExtendedSeeking (qnetwork.h)
author: windows-sdk-content
description: The IAMExtendedSeeking interface seeks to a marker in a Windows Media stream or changes the playback rate for a Windows Media file. This interface is implemented by the Windows Media Source filter and the WM ASF Reader filter.
old-location: dshow\iamextendedseeking.htm
tech.root: DirectShow
ms.assetid: 9e0e49af-61ef-408c-8c26-bb29ab26a1f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMExtendedSeeking, IAMExtendedSeeking interface [DirectShow], IAMExtendedSeeking interface [DirectShow],described, IAMExtendedSeekingInterface, dshow.iamextendedseeking, qnetwork/IAMExtendedSeeking
ms.topic: interface
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMExtendedSeeking
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtendedSeeking interface


## -description



The <code>IAMExtendedSeeking</code> interface seeks to a marker in a Windows Media stream or changes the playback rate for a Windows Media file. This interface is implemented by the <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter and the <a href="https://msdn.microsoft.com/82b9f849-b9dc-439b-8ca7-9dcd992338ab">WM ASF Reader</a> filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMExtendedSeeking</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMExtendedSeeking</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMExtendedSeeking</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389335(v=VS.85).aspx">get_CurrentMarker</a>
</td>
<td align="left" width="63%">
Retrieves the current marker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389336(v=VS.85).aspx">get_ExSeekCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the extended seeking capabilities of the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389337(v=VS.85).aspx">get_MarkerCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of markers in the current stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389338(v=VS.85).aspx">get_PlaybackSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the current playback speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389332(v=VS.85).aspx">GetMarkerName</a>
</td>
<td align="left" width="63%">
Retrieves the name associated with the specified marker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389334(v=VS.85).aspx">GetMarkerTime</a>
</td>
<td align="left" width="63%">
Retrieves the presentation time associated with the specified marker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389339(v=VS.85).aspx">put_PlaybackSpeed</a>
</td>
<td align="left" width="63%">
Sets the playback speed.

</td>
</tr>
</table> 


## -remarks



To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

