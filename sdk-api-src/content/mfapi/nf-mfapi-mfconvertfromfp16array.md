---
UID: NF:mfapi.MFConvertFromFP16Array
title: MFConvertFromFP16Array function (mfapi.h)
description: Converts an array of 16-bit floating-point numbers into an array of 32-bit floating-point numbers.
helpviewer_keywords: ["5cc11d32-8dcd-491d-b3df-c0b061233038","MFConvertFromFP16Array","MFConvertFromFP16Array function [Media Foundation]","mf.mfconvertfromfp16array","mfapi/MFConvertFromFP16Array"]
old-location: mf\mfconvertfromfp16array.htm
tech.root: mf
ms.assetid: 5cc11d32-8dcd-491d-b3df-c0b061233038
ms.date: 12/05/2018
ms.keywords: 5cc11d32-8dcd-491d-b3df-c0b061233038, MFConvertFromFP16Array, MFConvertFromFP16Array function [Media Foundation], mf.mfconvertfromfp16array, mfapi/MFConvertFromFP16Array
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
 - MFConvertFromFP16Array
 - mfapi/MFConvertFromFP16Array
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
 - MFConvertFromFP16Array
---

# MFConvertFromFP16Array function


## -description

Converts an array of 16-bit floating-point numbers into an array of 32-bit floating-point numbers.

## -parameters

### -param pDest [in]

Pointer to an array of <b>float</b> values. The array must contain at least <i>dwCount</i> elements.

### -param pSrc [in]

Pointer to an array of 16-bit floating-point values, typed as <b>WORD</b> values. The array must contain at least <i>dwCount</i> elements.

### -param dwCount [in]

Number of elements in the <i>pSrc</i> array to convert.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The function converts <i>dwCount</i> values in the <i>pSrc</i> array and writes them into the <i>pDest</i> array.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>