---
UID: NF:strmif.IEncoderAPI.GetParameterValues
title: IEncoderAPI::GetParameterValues
author: windows-sdk-content
description: The GetParameterValues method retrieves the list of values supported by the given parameter.
old-location: mstv\iencoderapi_getparametervalues.htm
old-project: mstv
ms.assetid: 406316b5-1de0-4a89-b1bc-2f3b63ab0739
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetParameterValues, GetParameterValues method [Microsoft TV Technologies], GetParameterValues method [Microsoft TV Technologies],IEncoderAPI interface, IEncoderAPI interface [Microsoft TV Technologies],GetParameterValues method, IEncoderAPI.GetParameterValues, IEncoderAPI::GetParameterValues, IEncoderAPIGetParameterValues, mstv.iencoderapi_getparametervalues, strmif/IEncoderAPI::GetParameterValues
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEncoderAPI.GetParameterValues
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IEncoderAPI::GetParameterValues


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>.]

The <b>GetParameterValues</b> method retrieves the list of values supported by the given parameter.


## -parameters




### -param Api [in]


            Pointer to a GUID that specifies the parameter.
          


### -param Values [out]


            Address of a pointer to an array that receives the values.
          


### -param ValuesCount [out]


            Indicates the number of entries placed into the array.
            




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns an array of <b>VARIANT</b> types representing the individual values supported by the parameter. This array is allocated by the callee through <b>CoTaskMemAlloc</b> and placed into the <i>Values</i> parameter. On exit, <i>ValuesCount</i> contains the number of elements in the array. The caller must free the array by calling <b>CoTaskMemFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI Interface</a>
 

 

