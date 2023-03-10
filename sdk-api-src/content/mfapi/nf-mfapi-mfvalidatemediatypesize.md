---
UID: NF:mfapi.MFValidateMediaTypeSize
title: MFValidateMediaTypeSize function (mfapi.h)
description: Validates the size of a buffer for a video format block.
helpviewer_keywords: ["782b59ca-bfa8-4217-9b72-50a78937775a","FORMAT_DvInfo","FORMAT_MFVideoFormat","FORMAT_MPEG2Video","FORMAT_MPEGStreams","FORMAT_MPEGVideo","FORMAT_VideoInfo","FORMAT_VideoInfo2","FORMAT_WaveFormatEx","MFValidateMediaTypeSize","MFValidateMediaTypeSize function [Media Foundation]","mf.mfvalidatemediatypesize","mfapi/MFValidateMediaTypeSize"]
old-location: mf\mfvalidatemediatypesize.htm
tech.root: mf
ms.assetid: 782b59ca-bfa8-4217-9b72-50a78937775a
ms.date: 12/05/2018
ms.keywords: 782b59ca-bfa8-4217-9b72-50a78937775a, FORMAT_DvInfo, FORMAT_MFVideoFormat, FORMAT_MPEG2Video, FORMAT_MPEGStreams, FORMAT_MPEGVideo, FORMAT_VideoInfo, FORMAT_VideoInfo2, FORMAT_WaveFormatEx, MFValidateMediaTypeSize, MFValidateMediaTypeSize function [Media Foundation], mf.mfvalidatemediatypesize, mfapi/MFValidateMediaTypeSize
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFValidateMediaTypeSize
 - mfapi/MFValidateMediaTypeSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFValidateMediaTypeSize
---

# MFValidateMediaTypeSize function


## -description

Validates the size of a buffer for a video format block.

## -parameters

### -param FormatType [in]

GUID that specifies the type of format block. It must be one of the following values:

<a id="FORMAT_DvInfo"></a>
<a id="format_dvinfo"></a>
<a id="FORMAT_DVINFO"></a>


#### FORMAT_DvInfo

<a id="FORMAT_MFVideoFormat"></a>
<a id="format_mfvideoformat"></a>
<a id="FORMAT_MFVIDEOFORMAT"></a>


#### FORMAT_MFVideoFormat

<a id="FORMAT_MPEG2Video"></a>
<a id="format_mpeg2video"></a>
<a id="FORMAT_MPEG2VIDEO"></a>


#### FORMAT_MPEG2Video

<a id="FORMAT_MPEGStreams"></a>
<a id="format_mpegstreams"></a>
<a id="FORMAT_MPEGSTREAMS"></a>


#### FORMAT_MPEGStreams

<a id="FORMAT_MPEGVideo"></a>
<a id="format_mpegvideo"></a>
<a id="FORMAT_MPEGVIDEO"></a>


#### FORMAT_MPEGVideo

<a id="FORMAT_VideoInfo"></a>
<a id="format_videoinfo"></a>
<a id="FORMAT_VIDEOINFO"></a>


#### FORMAT_VideoInfo

<a id="FORMAT_VideoInfo2"></a>
<a id="format_videoinfo2"></a>
<a id="FORMAT_VIDEOINFO2"></a>


#### FORMAT_VideoInfo2

<a id="FORMAT_WaveFormatEx"></a>
<a id="format_waveformatex"></a>
<a id="FORMAT_WAVEFORMATEX"></a>


#### FORMAT_WaveFormatEx

### -param pBlock [in]

Pointer to a buffer that contains the format block.

### -param cbSize [in]

Size of the <i>pBlock</i> buffer, in bytes.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The buffer that contains the format block is large enough.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The buffer that contains the format block is too small, or the format block is not valid.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
This function does not support the specified format type.
              

</td>
</tr>
</table>

## -remarks

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>