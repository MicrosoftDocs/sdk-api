---
UID: NF:mfapi.MFGetPlaneSize
title: MFGetPlaneSize function (mfapi.h)
description: Retrieves the image size, in bytes, for an uncompressed video format. (MFGetPlaneSize)
helpviewer_keywords: ["53ce83f3-b06e-4c91-a3e2-6369963e7810","MFGetPlaneSize","MFGetPlaneSize function [Media Foundation]","mf.mfgetplanesize","mfapi/MFGetPlaneSize"]
old-location: mf\mfgetplanesize.htm
tech.root: mf
ms.assetid: 53ce83f3-b06e-4c91-a3e2-6369963e7810
ms.date: 12/05/2018
ms.keywords: 53ce83f3-b06e-4c91-a3e2-6369963e7810, MFGetPlaneSize, MFGetPlaneSize function [Media Foundation], mf.mfgetplanesize, mfapi/MFGetPlaneSize
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
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetPlaneSize
 - mfapi/MFGetPlaneSize
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
 - MFGetPlaneSize
---

# MFGetPlaneSize function


## -description

Retrieves the image size, in bytes, for an uncompressed video format.

## -parameters

### -param format [in]

FOURCC code or <b>D3DFORMAT</b> value that specifies the video format.

### -param dwWidth [in]

Width of the image, in pixels.

### -param dwHeight [in]

Height of the image, in pixels.

### -param pdwPlaneSize [out]

Receives the size of one frame, in bytes. If the format is compressed or is not recognized, this value is zero.

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

This function is equivalent to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize">MFCalculateImageSize</a> function.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
