---
UID: NF:mfapi.MFConvertFromFP16Array
title: MFConvertFromFP16Array function
author: windows-driver-content
description: Converts an array of 16-bit floating-point numbers into an array of 32-bit floating-point numbers.
old-location: mf\mfconvertfromfp16array.htm
old-project: medfound
ms.assetid: 5cc11d32-8dcd-491d-b3df-c0b061233038
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 5cc11d32-8dcd-491d-b3df-c0b061233038, MFConvertFromFP16Array, MFConvertFromFP16Array function [Media Foundation], mf.mfconvertfromfp16array, mfapi/MFConvertFromFP16Array
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
-	MFConvertFromFP16Array
product: Windows
targetos: Windows
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The function converts <i>dwCount</i> values in the <i>pSrc</i> array and writes them into the <i>pDest</i> array.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="media_foundation_headers_and_libraries.htm">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

