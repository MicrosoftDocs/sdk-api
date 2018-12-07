---
UID: NN:mfmediaengine.IMFMediaSourceExtension
title: IMFMediaSourceExtension
author: windows-sdk-content
description: Provides functionality for the Media Source Extension (MSE).
old-location: mf\imfmediasourceextension.htm
tech.root: medfound
ms.assetid: 2acabcc2-242d-4b3d-b5b4-680c7973201f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFMediaSourceExtension, IMFMediaSourceExtension interface [Media Foundation], IMFMediaSourceExtension interface [Media Foundation],described, mf.imfmediasourceextension, mfmediaengine/IMFMediaSourceExtension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IMFMediaSourceExtension interface


## -description


Provides functionality for the Media Source Extension (MSE).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceExtension</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaSourceExtension</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1ecb7047-4dc9-4657-8a19-12108de299c0">AddSourceBuffer</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> to the collection of buffers associated with the <b>IMFMediaSourceExtension</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d4a70cf-7436-4f4a-9a7c-9127e3829ba8">GetActiveSourceBuffers</a>
</td>
<td align="left" width="63%">
Gets the source buffers that are actively supplying media data to the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0c644a0-9784-40b0-9d1f-7d9e8334d705">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the media source in 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/155d9202-5598-467c-b4d0-d22424b13b9d">GetReadyState</a>
</td>
<td align="left" width="63%">
Gets the ready state of the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ada32819-0ec3-4083-97a3-b8ae257d751b">GetSourceBuffer</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> at the specified index in the collection of buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/553b2711-1098-4e07-824d-42d5b2d57c16">GetSourceBuffers</a>
</td>
<td align="left" width="63%">
Gets the collection of source buffers associated with this media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/894ef7d2-d008-42e1-8a61-26f35a8877be">IsTypeSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the specified MIME type is supported by the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f29cbac-4261-41ee-84c8-cb73686aeee5">RemoveSourceBuffer</a>
</td>
<td align="left" width="63%">
Removes the specified source buffer from the collection of source buffers managed by the <b>IMFMediaSourceExtension</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc3dc600-ca81-40da-9edb-0af283ba9221">SetDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of the media source in 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d6bffcc-aa3c-4825-9268-00dcd2a347e6">SetEndOfStream</a>
</td>
<td align="left" width="63%">
Indicate that the end of the media stream has been reached. 

</td>
</tr>
</table> 


## -remarks



  Media Source Extensions (MSE) is a World Wide Web Consortium (W3C) standard that extends the HTML5 media  elements to enable dynamically changing the media stream without the use of plug-ins. The   <b>IMFMediaSourceExtension</b> interface  and the related Microsoft Win32 API implement MSE and are expected to only be called by web browsers implementing MSE.  

The MSE media source keeps track of the ready state of the of the source as well as a list of <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> objects which provide media data for the source.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

