---
UID: NF:mfapi.MFGetStrideForBitmapInfoHeader
title: MFGetStrideForBitmapInfoHeader function
author: windows-sdk-content
description: Calculates the minimum surface stride for a video format.
old-location: mf\mfgetstrideforbitmapinfoheader.htm
tech.root: medfound
ms.assetid: 09612b83-8b14-4286-9562-9e3d00fe2c2b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 09612b83-8b14-4286-9562-9e3d00fe2c2b, MFGetStrideForBitmapInfoHeader, MFGetStrideForBitmapInfoHeader function [Media Foundation], mf.mfgetstrideforbitmapinfoheader, mfapi/MFGetStrideForBitmapInfoHeader
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
 - MFGetStrideForBitmapInfoHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFGetStrideForBitmapInfoHeader
: 
---

# MFGetStrideForBitmapInfoHeader function


## -description


Calculates the minimum surface stride for a video format.
        


## -parameters




### -param format [in]

FOURCC code or <b>D3DFORMAT</b> value that specifies the video format. If you have a video subtype GUID, you can use the first <b>DWORD</b> of the subtype.


### -param dwWidth [in]

Width of the image, in pixels.


### -param pStride [out]

Receives the minimum surface stride, in pixels.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function calculates the minimum stride needed to hold the image in memory. Use this function if you are allocating buffers in system memory. Surfaces allocated in video memory might require a larger stride, depending on the graphics card.
      

If you are working with a DirectX surface buffer, use the <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">IMF2DBuffer::Lock2D</a> method to find the surface stride.
      

For planar YUV formats, this function returns the stride for the Y plane. Depending on the format, the chroma planes might have a different stride.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Ee663600(v=VS.85).aspx">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

