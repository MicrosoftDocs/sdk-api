---
UID: NF:mfapi.MFCreateAlignedMemoryBuffer
title: MFCreateAlignedMemoryBuffer function (mfapi.h)
description: Allocates system memory with a specified byte alignment and creates a media buffer to manage the memory.
helpviewer_keywords: ["MFCreateAlignedMemoryBuffer","MFCreateAlignedMemoryBuffer function [Media Foundation]","MF_128_BYTE_ALIGNMENT","MF_16_BYTE_ALIGNMENT","MF_1_BYTE_ALIGNMENT","MF_256_BYTE_ALIGNMENT","MF_2_BYTE_ALIGNMENT","MF_32_BYTE_ALIGNMENT","MF_4_BYTE_ALIGNMENT","MF_512_BYTE_ALIGNMENT","MF_64_BYTE_ALIGNMENT","MF_8_BYTE_ALIGNMENT","cccc0dea-3f1e-41e4-97f4-de7760ceccb0","mf.mfcreatealignedmemorybuffer","mfapi/MFCreateAlignedMemoryBuffer"]
old-location: mf\mfcreatealignedmemorybuffer.htm
tech.root: mf
ms.assetid: cccc0dea-3f1e-41e4-97f4-de7760ceccb0
ms.date: 12/05/2018
ms.keywords: MFCreateAlignedMemoryBuffer, MFCreateAlignedMemoryBuffer function [Media Foundation], MF_128_BYTE_ALIGNMENT, MF_16_BYTE_ALIGNMENT, MF_1_BYTE_ALIGNMENT, MF_256_BYTE_ALIGNMENT, MF_2_BYTE_ALIGNMENT, MF_32_BYTE_ALIGNMENT, MF_4_BYTE_ALIGNMENT, MF_512_BYTE_ALIGNMENT, MF_64_BYTE_ALIGNMENT, MF_8_BYTE_ALIGNMENT, cccc0dea-3f1e-41e4-97f4-de7760ceccb0, mf.mfcreatealignedmemorybuffer, mfapi/MFCreateAlignedMemoryBuffer
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
 - MFCreateAlignedMemoryBuffer
 - mfapi/MFCreateAlignedMemoryBuffer
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
 - MFCreateAlignedMemoryBuffer
---

# MFCreateAlignedMemoryBuffer function


## -description

Allocates system memory with a specified byte alignment and creates a media buffer to manage the memory.

## -parameters

### -param cbMaxLength

Size of the buffer, in bytes.

### -param cbAligment

Specifies the memory alignment for the buffer. Use one of the following constants.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_1_BYTE_ALIGNMENT"></a><a id="mf_1_byte_alignment"></a><dl>
<dt><b>MF_1_BYTE_ALIGNMENT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Align to 1 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_2_BYTE_ALIGNMENT"></a><a id="mf_2_byte_alignment"></a><dl>
<dt><b>MF_2_BYTE_ALIGNMENT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Align to 2 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_4_BYTE_ALIGNMENT"></a><a id="mf_4_byte_alignment"></a><dl>
<dt><b>MF_4_BYTE_ALIGNMENT</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Align to 4 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_8_BYTE_ALIGNMENT"></a><a id="mf_8_byte_alignment"></a><dl>
<dt><b>MF_8_BYTE_ALIGNMENT</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
Align to 8 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_16_BYTE_ALIGNMENT"></a><a id="mf_16_byte_alignment"></a><dl>
<dt><b>MF_16_BYTE_ALIGNMENT</b></dt>
<dt>0x0000000F</dt>
</dl>
</td>
<td width="60%">
Align to 16 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_32_BYTE_ALIGNMENT"></a><a id="mf_32_byte_alignment"></a><dl>
<dt><b>MF_32_BYTE_ALIGNMENT</b></dt>
<dt>0x0000001F</dt>
</dl>
</td>
<td width="60%">
Align to 32 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_64_BYTE_ALIGNMENT"></a><a id="mf_64_byte_alignment"></a><dl>
<dt><b>MF_64_BYTE_ALIGNMENT</b></dt>
<dt>0x0000003F</dt>
</dl>
</td>
<td width="60%">
Align to 64 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_128_BYTE_ALIGNMENT"></a><a id="mf_128_byte_alignment"></a><dl>
<dt><b>MF_128_BYTE_ALIGNMENT</b></dt>
<dt>0x0000007F</dt>
</dl>
</td>
<td width="60%">
Align to 128 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_256_BYTE_ALIGNMENT"></a><a id="mf_256_byte_alignment"></a><dl>
<dt><b>MF_256_BYTE_ALIGNMENT</b></dt>
<dt>0x000000FF</dt>
</dl>
</td>
<td width="60%">
Align to 256 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_512_BYTE_ALIGNMENT"></a><a id="mf_512_byte_alignment"></a><dl>
<dt><b>MF_512_BYTE_ALIGNMENT</b></dt>
<dt>0x000001FF</dt>
</dl>
</td>
<td width="60%">
Align to 512 bytes.
              

</td>
</tr>
</table>

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
</table>

## -remarks

When the media buffer object is destroyed, it releases the allocated memory.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer">MFCreateMemoryBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>