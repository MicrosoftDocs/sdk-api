---
UID: NF:mfapi.MFConvertColorInfoToDXVA
title: MFConvertColorInfoToDXVA function (mfapi.h)
author: windows-sdk-content
description: Converts the extended color information from an MFVIDEOFORMAT to the equivalent DirectX Video Acceleration (DXVA) color information.
old-location: mf\mfconvertcolorinfotodxva.htm
tech.root: medfound
ms.assetid: 52a3be2b-f715-4e12-9f69-6a832153ff5e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 52a3be2b-f715-4e12-9f69-6a832153ff5e, MFConvertColorInfoToDXVA, MFConvertColorInfoToDXVA function [Media Foundation], mf.mfconvertcolorinfotodxva, mfapi/MFConvertColorInfoToDXVA
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFConvertColorInfoToDXVA function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>.]

Converts the extended color information from an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a>  to the equivalent DirectX Video Acceleration (DXVA) color information.
        


## -parameters




### -param pdwToDXVA [out]

Receives the DXVA extended color information. The bitfields in the <b>DWORD</b> are defined in the <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure.


### -param pFromFormat [in]

Pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure that describes the video format.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Ee663600(v=VS.85).aspx">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

