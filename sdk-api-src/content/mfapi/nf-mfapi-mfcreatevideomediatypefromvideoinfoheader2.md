---
UID: NF:mfapi.MFCreateVideoMediaTypeFromVideoInfoHeader2
title: MFCreateVideoMediaTypeFromVideoInfoHeader2 function (mfapi.h)
author: windows-sdk-content
description: Creates a media type from a KS_VIDEOINFOHEADER2 structure.
old-location: mf\mfcreatevideomediatypefromvideoinfoheader2.htm
tech.root: medfound
ms.assetid: 2c0f4c47-7018-42f3-ae63-5209daa44158
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2c0f4c47-7018-42f3-ae63-5209daa44158, MFCreateVideoMediaTypeFromVideoInfoHeader2, MFCreateVideoMediaTypeFromVideoInfoHeader2 function [Media Foundation], mf.mfcreatevideomediatypefromvideoinfoheader2, mfapi/MFCreateVideoMediaTypeFromVideoInfoHeader2
ms.topic: function
f1_keywords:
- mfapi/MFCreateVideoMediaTypeFromVideoInfoHeader2
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
- MFCreateVideoMediaTypeFromVideoInfoHeader2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Bitwise <b>OR</b> of flags from the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoflags">MFVideoFlags</a> enumeration. Use this parameter for format information that is not contained in the <b>KS_VIDEOINFOHEADER2</b> structure.


### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>KS_VIDEOINFOHEADER2</b> structure.


### -param ppIVideoMediaType

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>
 

 

