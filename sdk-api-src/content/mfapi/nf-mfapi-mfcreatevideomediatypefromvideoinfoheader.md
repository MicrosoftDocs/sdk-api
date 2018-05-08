---
UID: NF:mfapi.MFCreateVideoMediaTypeFromVideoInfoHeader
title: MFCreateVideoMediaTypeFromVideoInfoHeader function
author: windows-driver-content
description: Creates a media type from a KS_VIDEOINFOHEADER structure.
old-location: mf\mfcreatevideomediatypefromvideoinfoheader.htm
old-project: medfound
ms.assetid: 922ab0b5-2363-4073-9252-a71b79e03573
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 922ab0b5-2363-4073-9252-a71b79e03573, MFCreateVideoMediaTypeFromVideoInfoHeader, MFCreateVideoMediaTypeFromVideoInfoHeader function [Media Foundation], mf.mfcreatevideomediatypefromvideoinfoheader, mfapi/MFCreateVideoMediaTypeFromVideoInfoHeader
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateVideoMediaTypeFromVideoInfoHeader
product: Windows
targetos: Windows
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateVideoMediaTypeFromVideoInfoHeader function


## -description



          Creates a media type from a <b>KS_VIDEOINFOHEADER</b> structure.
        


## -parameters




### -param pVideoInfoHeader

Pointer to the <b>KS_VIDEOINFOHEADER</b> structure to convert. (This structure is identical to the DirectShow <b>VIDEOINFOHEADER</b> structure.)


### -param cbVideoInfoHeader

Size of the <b>KS_VIDEOINFOHEADER</b> structure in bytes.


### -param dwPixelAspectRatioX

The X dimension of the pixel aspect ratio. The pixel aspect ratio is <i>dwPixelAspectRatioX</i>:<i>dwPixelAspectRatioY</i>.


### -param dwPixelAspectRatioY

The Y dimension of the pixel aspect ratio.


### -param InterlaceMode

Member of the <a href="https://msdn.microsoft.com/10a3d7b1-74ed-46cd-b10e-59a8f01726d5">MFVideoInterlaceMode</a> enumeration that specifies how the video is interlaced.


### -param VideoFlags

Bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/2530bf1d-05b1-4c16-b00b-117c0dadb301">MFVideoFlags</a> enumeration.


### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>KS_VIDEOINFOHEADER</b> structure.


### -param ppIVideoMediaType

Receives a pointer to the <a href="https://msdn.microsoft.com/9109b0dd-c44d-41d4-9480-1ca5c667dbd7">IMFVideoMediaType</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="media_foundation_headers_and_libraries.htm">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

