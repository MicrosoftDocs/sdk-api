---
UID: NN:mfmediaengine.IMFMediaSourceExtension
title: IMFMediaSourceExtension (mfmediaengine.h)
author: windows-sdk-content
description: Provides functionality for the Media Source Extension (MSE).
old-location: mf\imfmediasourceextension.htm
tech.root: medfound
ms.assetid: 2acabcc2-242d-4b3d-b5b4-680c7973201f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaSourceExtension, IMFMediaSourceExtension interface [Media Foundation], IMFMediaSourceExtension interface [Media Foundation],described, mf.imfmediasourceextension, mfmediaengine/IMFMediaSourceExtension
ms.topic: interface
f1_keywords: ["mfmediaengine/IMFMediaSourceExtension"]
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFMediaSourceExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSourceExtension interface


## -description


Provides functionality for the Media Source Extension (MSE).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceExtension</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaSourceExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourceExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediasourceextension-addsourcebuffer">AddSourceBuffer</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> to the collection of buffers associated with the <b>IMFMediaSourceExtension</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediasourceextension-getactivesourcebuffers">GetActiveSourceBuffers</a>
</td>
<td align="left" width="63%">
Gets the source buffers that are actively supplying media data to the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediasourceextension-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the media source in 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediasourceextension-getreadystate">GetReadyState</a>
</td>
<td align="left" width="63%">
Gets the ready state of the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediasourceextension-getsourcebuffer">GetSourceBuffer</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> at the specified index in the collection of buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediasourceextension-getsourcebuffers">GetSourceBuffers</a>
</td>
<td align="left" width="63%">
Gets the collection of source buffers associated with this media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediasourceextension-istypesupported">IsTypeSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the specified MIME type is supported by the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediasourceextension-removesourcebuffer">RemoveSourceBuffer</a>
</td>
<td align="left" width="63%">
Removes the specified source buffer from the collection of source buffers managed by the <b>IMFMediaSourceExtension</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediasourceextension-setduration">SetDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of the media source in 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediasourceextension-setendofstream">SetEndOfStream</a>
</td>
<td align="left" width="63%">
Indicate that the end of the media stream has been reached. 

</td>
</tr>
</table> 


## -remarks



  Media Source Extensions (MSE) is a World Wide Web Consortium (W3C) standard that extends the HTML5 media  elements to enable dynamically changing the media stream without the use of plug-ins. The   <b>IMFMediaSourceExtension</b> interface  and the related Microsoft Win32 API implement MSE and are expected to only be called by web browsers implementing MSE.  

The MSE media source keeps track of the ready state of the of the source as well as a list of <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> objects which provide media data for the source.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

