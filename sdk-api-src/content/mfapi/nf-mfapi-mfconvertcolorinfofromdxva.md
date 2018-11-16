---
UID: NF:mfapi.MFConvertColorInfoFromDXVA
title: MFConvertColorInfoFromDXVA function
author: windows-sdk-content
description: Sets the extended color information in a MFVIDEOFORMAT structure.
old-location: mf\mfconvertcolorinfofromdxva.htm
tech.root: medfound
ms.assetid: b16874cc-1eb3-43dd-bd4c-3ea77be10bd2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MFConvertColorInfoFromDXVA, MFConvertColorInfoFromDXVA function [Media Foundation], b16874cc-1eb3-43dd-bd4c-3ea77be10bd2, mf.mfconvertcolorinfofromdxva, mfapi/MFConvertColorInfoFromDXVA
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MFConvertColorInfoFromDXVA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFConvertColorInfoFromDXVA
: 
---

# MFConvertColorInfoFromDXVA function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>.]

Sets the extended color information in a <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.


## -parameters




### -param pToFormat [in, out]

Pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure. The function fills in the structure members that correspond to the DXVA color information in the <i>dwFromDXVA</i> parameter. The function does not modify the other structure members.


### -param dwFromDXVA [in]

<b>DWORD</b> that contains extended color information. The bitfields in the <b>DWORD</b> are defined in the <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function sets the following fields in the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.

<ul>
<li><b>videoInfo.MFNominalRange</b></li>
<li><b>videoInfo.MFVideoLighting</b></li>
<li><b>videoInfo.MFVideoPrimaries</b></li>
<li><b>videoInfo.MFVideoTransferFunction</b></li>
<li><b>videoInfo.MFVideoTransferMatrix</b></li>
<li><b>videoInfo.SourceChromaSubsampling</b></li>
</ul>
<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Ee663600(v=VS.85).aspx">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

