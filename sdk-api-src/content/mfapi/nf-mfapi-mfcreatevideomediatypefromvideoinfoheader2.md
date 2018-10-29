---
UID: NF:mfapi.MFCreateVideoMediaTypeFromVideoInfoHeader2
title: MFCreateVideoMediaTypeFromVideoInfoHeader2 function
author: windows-sdk-content
description: Creates a media type from a KS_VIDEOINFOHEADER2 structure.
old-location: mf\mfcreatevideomediatypefromvideoinfoheader2.htm
tech.root: medfound
ms.assetid: 2c0f4c47-7018-42f3-ae63-5209daa44158
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 2c0f4c47-7018-42f3-ae63-5209daa44158, MFCreateVideoMediaTypeFromVideoInfoHeader2, MFCreateVideoMediaTypeFromVideoInfoHeader2 function [Media Foundation], mf.mfcreatevideomediatypefromvideoinfoheader2, mfapi/MFCreateVideoMediaTypeFromVideoInfoHeader2
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
 - MFCreateVideoMediaTypeFromVideoInfoHeader2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateVideoMediaTypeFromVideoInfoHeader2 function


## -description


Creates a media type from a <b>KS_VIDEOINFOHEADER2</b> structure.
        


## -parameters




### -param pVideoInfoHeader

Pointer to the <b>KS_VIDEOINFOHEADER2</b> structure to convert. (This structure is identical to the DirectShow <b>VIDEOINFOHEADER2</b> structure.)


### -param cbVideoInfoHeader

Size of the <b>KS_VIDEOINFOHEADER2</b> structure in bytes.


### -param AdditionalVideoFlags

Bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/2530bf1d-05b1-4c16-b00b-117c0dadb301">MFVideoFlags</a> enumeration. Use this parameter for format information that is not contained in the <b>KS_VIDEOINFOHEADER2</b> structure.


### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>KS_VIDEOINFOHEADER2</b> structure.


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
 

 

