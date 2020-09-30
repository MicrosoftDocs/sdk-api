---
UID: NF:mfapi.MFCreateMemoryBuffer
title: MFCreateMemoryBuffer function (mfapi.h)
description: Allocates system memory and creates a media buffer to manage it.
helpviewer_keywords: ["1f79d057-7ef7-4662-9f82-ceadc23276f0","MFCreateMemoryBuffer","MFCreateMemoryBuffer function [Media Foundation]","mf.mfcreatememorybuffer","mfapi/MFCreateMemoryBuffer"]
old-location: mf\mfcreatememorybuffer.htm
tech.root: mf
ms.assetid: 1f79d057-7ef7-4662-9f82-ceadc23276f0
ms.date: 12/05/2018
ms.keywords: 1f79d057-7ef7-4662-9f82-ceadc23276f0, MFCreateMemoryBuffer, MFCreateMemoryBuffer function [Media Foundation], mf.mfcreatememorybuffer, mfapi/MFCreateMemoryBuffer
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
 - MFCreateMemoryBuffer
 - mfapi/MFCreateMemoryBuffer
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
 - MFCreateMemoryBuffer
---

# MFCreateMemoryBuffer function


## -description

Allocates system memory and creates a media buffer to manage it.

## -parameters

### -param cbMaxLength

Size of the buffer, in bytes.

### -param ppBuffer

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of the media buffer. The caller must release the interface.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -remarks

The function allocates a buffer with a 1-byte memory alignment. To allocate a buffer that is aligned to a larger memory boundary, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer">MFCreateAlignedMemoryBuffer</a>.

When the media buffer object is destroyed, it releases the allocated memory.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>