---
UID: NF:mfapi.MFCreateMediaBufferWrapper
title: MFCreateMediaBufferWrapper function (mfapi.h)
description: Creates a media buffer that wraps an existing media buffer.
helpviewer_keywords: ["6850e75c-4612-4514-a74d-9b36fd88a598","MFCreateMediaBufferWrapper","MFCreateMediaBufferWrapper function [Media Foundation]","mf.mfcreatemediabufferwrapper","mfapi/MFCreateMediaBufferWrapper"]
old-location: mf\mfcreatemediabufferwrapper.htm
tech.root: mf
ms.assetid: 6850e75c-4612-4514-a74d-9b36fd88a598
ms.date: 12/05/2018
ms.keywords: 6850e75c-4612-4514-a74d-9b36fd88a598, MFCreateMediaBufferWrapper, MFCreateMediaBufferWrapper function [Media Foundation], mf.mfcreatemediabufferwrapper, mfapi/MFCreateMediaBufferWrapper
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFCreateMediaBufferWrapper
 - mfapi/MFCreateMediaBufferWrapper
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
 - MFCreateMediaBufferWrapper
---

# MFCreateMediaBufferWrapper function


## -description

Creates a media buffer that wraps an existing media buffer. The new media buffer points to the same memory as the original media buffer, or to an offset from the start of the memory.

## -parameters

### -param pBuffer [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of the original media buffer.

### -param cbOffset [in]

The start of the new buffer, as an offset in bytes from the start of the original buffer.

### -param dwLength [in]

The size of the new buffer. The value of <i>cbOffset</i> + <i>dwLength</i> must be less than or equal to the size of valid data the original buffer. (The size of the valid data is returned by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength">IMFMediaBuffer::GetCurrentLength</a> method.)

### -param ppBuffer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface. The caller must release the interface.

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
The function succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The requested offset or the requested length is not valid.
              

</td>
</tr>
</table>

## -remarks

The maximum size of the wrapper buffer is limited to the size of the valid data in the original buffer. This might be less than the allocated size of the original buffer. To set the size of the valid data, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength">IMFMediaBuffer::SetCurrentLength</a>.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>