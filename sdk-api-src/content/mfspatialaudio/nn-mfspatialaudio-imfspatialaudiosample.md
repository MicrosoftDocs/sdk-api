---
UID: NN:mfspatialaudio.IMFSpatialAudioSample
title: IMFSpatialAudioSample
author: windows-sdk-content
description: Represents a multimedia sample with spatial sound information. Every IMFSpatialAudioSample contains one or more IMFSpatialAudioObjectBuffer objects.
old-location: mf\imfspatialaudiosample.htm
tech.root: medfound
ms.assetid: EA0277BF-C9C8-42FE-9206-A87FC3C50A9F
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IMFSpatialAudioSample, IMFSpatialAudioSample interface [Media Foundation], IMFSpatialAudioSample interface [Media Foundation],described, mf.imfspatialaudiosample, mfspatialaudio/IMFSpatialAudioSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSpatialAudioSample interface


## -description


Represents a multimedia sample with spatial sound information. Every <b>IMFSpatialAudioSample</b> contains one or more <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSpatialAudioSample</b> interface inherits from <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>. <b>IMFSpatialAudioSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSpatialAudioSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D967B4FE-8E11-4520-BF9E-725ACC7AA99A">AddSpatialAudioObject</a>
</td>
<td align="left" width="63%">
Adds a new spatial audio object, represented by an <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> object, to the     sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D386E482-4C5A-4F8A-801F-EA1AD4C9157C">GetObjectCount</a>
</td>
<td align="left" width="63%">
Gets the count of spatial audio objects, represented by <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> objects, in the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B5A2D44-BA41-49FC-B4FD-9BCD9EE2D549">GetSpatialAudioObjectByIndex</a>
</td>
<td align="left" width="63%">
Returns the spatial audio object, represented by an <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> object, corresponding to the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>
 

 

