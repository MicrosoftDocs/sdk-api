---
UID: NF:mfapi.MFCalculateBitmapImageSize
title: MFCalculateBitmapImageSize function (mfapi.h)
description: Retrieves the image size for a video format.
helpviewer_keywords: ["67d80db8-996e-4f59-82f0-efd3d4bd8ff0","MFCalculateBitmapImageSize","MFCalculateBitmapImageSize function [Media Foundation]","mf.mfcalculatebitmapimagesize","mfapi/MFCalculateBitmapImageSize"]
old-location: mf\mfcalculatebitmapimagesize.htm
tech.root: mf
ms.assetid: 67d80db8-996e-4f59-82f0-efd3d4bd8ff0
ms.date: 12/05/2018
ms.keywords: 67d80db8-996e-4f59-82f0-efd3d4bd8ff0, MFCalculateBitmapImageSize, MFCalculateBitmapImageSize function [Media Foundation], mf.mfcalculatebitmapimagesize, mfapi/MFCalculateBitmapImageSize
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
 - MFCalculateBitmapImageSize
 - mfapi/MFCalculateBitmapImageSize
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
 - MFCalculateBitmapImageSize
---

# MFCalculateBitmapImageSize function


## -description

Retrieves the image size for a video format. Given a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure, this function calculates the correct value of the <b>biSizeImage</b> member.

## -parameters

### -param pBMIH [in]

Pointer to a <b>BITMAPINFOHEADER</b> structure that describes the format.

### -param cbBufSize [in]

Size of the <i>pBMIH</i> buffer, in bytes. The size includes any color masks or palette entries that follow the <b>BITMAPINFOHEADER</b> structure.

### -param pcbImageSize [out]

Receives the image size, in bytes.

### -param pbKnown [out]

Receives the value <b>TRUE</b> if the function recognizes the video format. Otherwise, receives the value <b>FALSE</b>. This parameter can be <b>NULL</b>.

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
The <b>BITMAPINFOHEADER</b> structure is not valid, or the value of <i>cbBufSize</i> is too small.
              

</td>
</tr>
</table>

## -remarks

Before calling this function, you must set at least the following members of the <b>BITMAPINFOHEADER</b> structure:

<ul>
<li><b>biCompression</b></li>
<li><b>biBitCount</b></li>
<li><b>biWidth</b></li>
<li><b>biHeight</b></li>
</ul>
Also, if <b>biCompression</b> is <b>BI_BITFIELDS</b>, the <b>BITMAPINFOHEADER</b> structure must be followed by an array of color masks.
      

This function fails if the <b>BITMAPINFOHEADER</b> structure describes a format that is not a video format. For example, it fails if <b>biCompresson</b> is <b>BI_JPEG</b> or <b>BI_PNG</b> .

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>