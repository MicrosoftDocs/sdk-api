---
UID: NN:mfmediaengine.IMFSourceBuffer
title: IMFSourceBuffer (mfmediaengine.h)

description: Represents a buffer which contains media data for a IMFMediaSourceExtension.
old-location: mf\imfsourcebuffer.htm
tech.root: medfound
ms.assetid: f241e232-9013-46d0-be97-2d6b5246cff3

ms.date: 12/05/2018
ms.keywords: IMFSourceBuffer, IMFSourceBuffer interface [Media Foundation], IMFSourceBuffer interface [Media Foundation],described, mf.imfsourcebuffer, mfmediaengine/IMFSourceBuffer
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFSourceBuffer"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceBuffer interface


## -description


Represents a buffer which contains media data for a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceBuffer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffer-abort">Abort</a>
</td>
<td align="left" width="63%">
Aborts the processing of the current media segment. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffer-append">Append</a>
</td>
<td align="left" width="63%">
Appends the specified media segment to the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-appendbytestream">AppendByteStream</a>
</td>
<td align="left" width="63%">
Appends the media segment from the specified byte stream to the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-getappendwindowend">GetAppendWindowEnd</a>
</td>
<td align="left" width="63%">
Gets the timestamp for the end of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-getappendwindowstart">GetAppendWindowStart</a>
</td>
<td align="left" width="63%">
Gets the timestamp for the start of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-getbuffered">GetBuffered</a>
</td>
<td align="left" width="63%">
Gets the buffered time range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-gettimestampoffset">GetTimeStampOffset</a>
</td>
<td align="left" width="63%">
Gets the timestamp offset for media segments appended to the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-getupdating">GetUpdating</a>
</td>
<td align="left" width="63%">
Gets a value that indicates  if <a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffer-append">Append</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-appendbytestream">AppendByteStream</a>, or <a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffer-remove">Remove</a> is in process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffer-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes the media segments defined by the specified time range from the <b>IMFSourceBuffer</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-setappendwindowend">SetAppendWindowEnd</a>
</td>
<td align="left" width="63%">
Sets the timestamp for the end of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-setappendwindowstart">SetAppendWindowStart</a>
</td>
<td align="left" width="63%">
Sets the timestamp for the start of the append window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffer-settimestampoffset">SetTimeStampOffset</a>
</td>
<td align="left" width="63%">
Sets the timestamp offset for media segments appended to the <b>IMFSourceBuffer</b>.

</td>
</tr>
</table> 


## -remarks



<b>IMFSourceBuffer</b> is used in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

