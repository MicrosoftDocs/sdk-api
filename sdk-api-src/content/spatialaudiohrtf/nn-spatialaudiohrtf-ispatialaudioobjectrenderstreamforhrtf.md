---
UID: NN:spatialaudiohrtf.ISpatialAudioObjectRenderStreamForHrtf
title: ISpatialAudioObjectRenderStreamForHrtf (spatialaudiohrtf.h)
author: windows-sdk-content
description: Provides methods for controlling an Hrtf spatial audio object render stream, including starting, stopping, and resetting the stream.
old-location: coreaudio\ispatialaudiorenderstreamforhrtf.htm
tech.root: CoreAudio
ms.assetid: 9DFEF82A-1571-47AB-BE0E-059BCCC8289A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamForHrtf, ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio], ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio],described, coreaudio.ispatialaudiorenderstreamforhrtf, spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf
ms.topic: interface
f1_keywords: 
 - "spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf"
req.header: spatialaudiohrtf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - spatialaudiohrtf.h
api_name:
 - ISpatialAudioObjectRenderStreamForHrtf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioObjectRenderStreamForHrtf interface


## -description


Provides methods for controlling an Hrtf spatial audio object render stream, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectRenderStreamForHrtf</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a>. <b>ISpatialAudioObjectRenderStreamForHrtf</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectRenderStreamForHrtf</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf">ActivateSpatialAudioObjectForHrtf</a>
</td>
<td align="left" width="63%">
Activates an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> for audio rendering.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a>
 

 

