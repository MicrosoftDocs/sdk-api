---
UID: NF:mfapi.MFConvertColorInfoFromDXVA
title: MFConvertColorInfoFromDXVA function (mfapi.h)
description: Sets the extended color information in a MFVIDEOFORMAT structure.
helpviewer_keywords: ["MFConvertColorInfoFromDXVA","MFConvertColorInfoFromDXVA function [Media Foundation]","b16874cc-1eb3-43dd-bd4c-3ea77be10bd2","mf.mfconvertcolorinfofromdxva","mfapi/MFConvertColorInfoFromDXVA"]
old-location: mf\mfconvertcolorinfofromdxva.htm
tech.root: mf
ms.assetid: b16874cc-1eb3-43dd-bd4c-3ea77be10bd2
ms.date: 12/05/2018
ms.keywords: MFConvertColorInfoFromDXVA, MFConvertColorInfoFromDXVA function [Media Foundation], b16874cc-1eb3-43dd-bd4c-3ea77be10bd2, mf.mfconvertcolorinfofromdxva, mfapi/MFConvertColorInfoFromDXVA
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
 - MFConvertColorInfoFromDXVA
 - mfapi/MFConvertColorInfoFromDXVA
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
 - MFConvertColorInfoFromDXVA
---

# MFConvertColorInfoFromDXVA function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>.]

Sets the extended color information in a <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -parameters

### -param pToFormat [in, out]

Pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure. The function fills in the structure members that correspond to the DXVA color information in the <i>dwFromDXVA</i> parameter. The function does not modify the other structure members.

### -param dwFromDXVA [in]

<b>DWORD</b> that contains extended color information. The bitfields in the <b>DWORD</b> are defined in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function sets the following fields in the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

<ul>
<li><b>videoInfo.MFNominalRange</b></li>
<li><b>videoInfo.MFVideoLighting</b></li>
<li><b>videoInfo.MFVideoPrimaries</b></li>
<li><b>videoInfo.MFVideoTransferFunction</b></li>
<li><b>videoInfo.MFVideoTransferMatrix</b></li>
<li><b>videoInfo.SourceChromaSubsampling</b></li>
</ul>
<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>