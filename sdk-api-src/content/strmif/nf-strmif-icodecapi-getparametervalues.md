---
UID: NF:strmif.ICodecAPI.GetParameterValues
title: ICodecAPI::GetParameterValues
author: windows-sdk-content
description: The GetParameterValues method gets the list of possible values for a codec property.
old-location: dshow\icodecapi_getparametervalues.htm
tech.root: DirectShow
ms.assetid: 7f6c7db8-f71f-4ea7-8584-0df6e28c0fc9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetParameterValues, GetParameterValues method [DirectShow], GetParameterValues method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetParameterValues method, ICodecAPI.GetParameterValues, ICodecAPI::GetParameterValues, ICodecAPIGetParameterValues, dshow.icodecapi_getparametervalues, strmif/ICodecAPI::GetParameterValues
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICodecAPI.GetParameterValues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICodecAPI::GetParameterValues


## -description


The <b>GetParameterValues</b> method gets the list of possible values for a codec property.

This method applies only to properties that support a list of possible values, as opposed to a linear range.


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the property to query. For a list of standard codec properties, see <a href="https://msdn.microsoft.com/5d527af7-07cf-42e2-99bb-d56c856cc1bc">Codec API Properties</a>.
          


### -param Values [out]

Receives a pointer to an array of <b>VARIANT</b> types. The array contains the list of values that the encoder supports for this property. The caller must free each <b>VARIANT</b> by calling <b>VariantClear</b>. The caller must also free the array by calling  <b>CoTaskMemFree</b>.
          


### -param ValuesCount [out]

Receives the number of elements in the <i>Values</i> array.
          


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CODECAPI_LINEAR_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The property supports a range of values, not a list.

</td>
</tr>
</table>
 




## -remarks



If the property supports a range of values, instead of a list, the method returns  <b>VFW_E_CODECAPI_LINEAR_RANGE</b>. In that case, call <a href="https://msdn.microsoft.com/35bf758f-0ce3-4b3a-aae5-9d4326089743">ICodecAPI::GetParameterRange</a> to get the range of values.
      




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>
 

 

