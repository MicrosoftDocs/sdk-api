---
UID: NN:mfmediaengine.IMFSourceBuffer
title: IMFSourceBuffer (mfmediaengine.h)
author: windows-sdk-content
description: Represents a buffer which contains media data for a IMFMediaSourceExtension.
old-location: mf\imfsourcebuffer.htm
tech.root: medfound
ms.assetid: f241e232-9013-46d0-be97-2d6b5246cff3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSourceBuffer, IMFSourceBuffer interface [Media Foundation], IMFSourceBuffer interface [Media Foundation],described, mf.imfsourcebuffer, mfmediaengine/IMFSourceBuffer
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
 - IMFSourceBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceBuffer interface


## -description


Represents a buffer which contains media data for a <a href="https://msdn.microsoft.com/2acabcc2-242d-4b3d-b5b4-680c7973201f">IMFMediaSourceExtension</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSourceBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31253d0d-c53f-47bd-823a-fc564cb63b78">Abort</a>
</td>
<td align="left" width="63%">
Aborts the processing of the current media segment. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/824fa23d-57d9-411a-af8a-fb65dca124b2">Append</a>
</td>
<td align="left" width="63%">
Appends the specified media segment to the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a4fc611-4923-48ad-bc92-c3686d855c13">AppendByteStream</a>
</td>
<td align="left" width="63%">
Appends the media segment from the specified byte stream to the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac9806ca-8529-48be-8b5a-ae0126d8554d">GetAppendWindowEnd</a>
</td>
<td align="left" width="63%">
Gets the timestamp for the end of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5feb451-5bf9-475c-b501-599e2188a3f5">GetAppendWindowStart</a>
</td>
<td align="left" width="63%">
Gets the timestamp for the start of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbed0e90-8950-46f6-acaa-5e6daf814dd0">GetBuffered</a>
</td>
<td align="left" width="63%">
Gets the buffered time range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb8a237b-2602-40ad-921e-3b76fbac3ea8">GetTimeStampOffset</a>
</td>
<td align="left" width="63%">
Gets the timestamp offset for media segments appended to the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1c810d1-05dd-4931-b063-fb86c6bedae3">GetUpdating</a>
</td>
<td align="left" width="63%">
Gets a value that indicates  if <a href="https://msdn.microsoft.com/824fa23d-57d9-411a-af8a-fb65dca124b2">Append</a>, <a href="https://msdn.microsoft.com/1a4fc611-4923-48ad-bc92-c3686d855c13">AppendByteStream</a>, or <a href="https://msdn.microsoft.com/86536d73-18c0-4acc-81ec-72f1dfe400c5">Remove</a> is in process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86536d73-18c0-4acc-81ec-72f1dfe400c5">Remove</a>
</td>
<td align="left" width="63%">
Removes the media segments defined by the specified time range from the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80cae375-b3f4-4947-98dd-26338d4a0486">SetAppendWindowEnd</a>
</td>
<td align="left" width="63%">
Sets the timestamp for the end of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f78e53c-ea2b-4849-9d01-6c31539d8ef5">SetAppendWindowStart</a>
</td>
<td align="left" width="63%">
Sets the timestamp for the start of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db905149-f6f2-445e-87bb-6705a1a078eb">SetTimeStampOffset</a>
</td>
<td align="left" width="63%">
Sets the timestamp offset for media segments appended to the <b>IMFSourceBuffer</b>.

</td>
</tr>
</table> 


## -remarks



<b>IMFSourceBuffer</b> is used in conjunction with the <a href="https://msdn.microsoft.com/2acabcc2-242d-4b3d-b5b4-680c7973201f">IMFMediaSourceExtension</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

