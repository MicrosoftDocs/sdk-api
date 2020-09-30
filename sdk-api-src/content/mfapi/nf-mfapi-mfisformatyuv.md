---
UID: NF:mfapi.MFIsFormatYUV
title: MFIsFormatYUV function (mfapi.h)
description: Queries whether a FOURCC code or D3DFORMAT value is a YUV format.
helpviewer_keywords: ["MFIsFormatYUV","MFIsFormatYUV function [Media Foundation]","dbf6acd3-79c6-4ec2-a867-f2b2d8b41f53","mf.mfisformatyuv","mfapi/MFIsFormatYUV"]
old-location: mf\mfisformatyuv.htm
tech.root: mf
ms.assetid: dbf6acd3-79c6-4ec2-a867-f2b2d8b41f53
ms.date: 12/05/2018
ms.keywords: MFIsFormatYUV, MFIsFormatYUV function [Media Foundation], dbf6acd3-79c6-4ec2-a867-f2b2d8b41f53, mf.mfisformatyuv, mfapi/MFIsFormatYUV
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
req.dll: Evr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFIsFormatYUV
 - mfapi/MFIsFormatYUV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - evr.dll
api_name:
 - MFIsFormatYUV
---

# MFIsFormatYUV function


## -description

Queries whether a FOURCC code or <b>D3DFORMAT</b> value is a YUV format.

## -parameters

### -param Format [in]

FOURCC code or <b>D3DFORMAT</b> value.

## -returns

The function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The value specifies a YUV format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The value does not specify a recognized YUV format.

</td>
</tr>
</table>

## -remarks

This function checks whether <i>Format</i> specifies a YUV format. Not every YUV format is recognized by this function. However, if a YUV format is not recognized by this function, it is probably not supported for video rendering or DirectX video acceleration (DXVA).

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>