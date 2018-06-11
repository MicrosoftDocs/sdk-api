---
UID: NF:mfapi.MFCopyImage
title: MFCopyImage function
author: windows-sdk-content
description: Copies an image or image plane from one buffer to another.
old-location: mf\mfcopyimage.htm
old-project: medfound
ms.assetid: e6bc2777-d33c-4d44-84c6-e7b35d308d33
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCopyImage, MFCopyImage function [Media Foundation], e6bc2777-d33c-4d44-84c6-e7b35d308d33, mf.mfcopyimage, mfapi/MFCopyImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCopyImage
product: Windows
targetos: Windows
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCopyImage function


## -description



          Copies an image or image plane from one buffer to another.
        


## -parameters




### -param pDest [in]


            Pointer to the start of the first row of pixels in the destination buffer.
          


### -param lDestStride [in]


            Stride of the destination buffer, in bytes.
          


### -param pSrc [in]


            Pointer to the start of the first row of pixels in the source image.
          


### -param lSrcStride [in]


            Stride of the source image, in bytes.
          


### -param dwWidthInBytes [in]


            Width of the image, in bytes.
          


### -param dwLines [in]


            Number of rows of pixels to copy.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        This function copies a single plane of the image. For planar YUV formats, you must call the function once for each plane. In this case, <i>pDest</i> and <i>pSrc</i> must point to the start of each plane.
      


        This function is optimized if the MMX, SSE, or SSE2 instruction sets are available on the processor. The function performs a non-temporal store (the data is written to memory directly without polluting the cache).
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="media_foundation_headers_and_libraries.htm">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

