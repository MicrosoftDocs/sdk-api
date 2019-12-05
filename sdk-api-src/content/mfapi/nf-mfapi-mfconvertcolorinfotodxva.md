---
UID: NF:mfapi.MFConvertColorInfoToDXVA
title: MFConvertColorInfoToDXVA function (mfapi.h)
description: Converts the extended color information from an MFVIDEOFORMAT to the equivalent DirectX Video Acceleration (DXVA) color information.
old-location: mf\mfconvertcolorinfotodxva.htm
tech.root: medfound
ms.assetid: 52a3be2b-f715-4e12-9f69-6a832153ff5e
ms.date: 12/05/2018
ms.keywords: 52a3be2b-f715-4e12-9f69-6a832153ff5e, MFConvertColorInfoToDXVA, MFConvertColorInfoToDXVA function [Media Foundation], mf.mfconvertcolorinfotodxva, mfapi/MFConvertColorInfoToDXVA
ms.topic: function
f1_keywords:
- mfapi/MFConvertColorInfoToDXVA
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mfplat.dll
api_name:
- MFConvertColorInfoToDXVA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFConvertColorInfoToDXVA function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/extended-color-information">Extended Color Information</a>.]

Converts the extended color information from an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a>  to the equivalent DirectX Video Acceleration (DXVA) color information.
        


## -parameters




### -param pdwToDXVA [out]

Receives the DXVA extended color information. The bitfields in the <b>DWORD</b> are defined in the <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure.


### -param pFromFormat [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure that describes the video format.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>
 

 

