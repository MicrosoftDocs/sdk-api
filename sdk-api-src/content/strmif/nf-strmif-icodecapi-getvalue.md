---
UID: NF:strmif.ICodecAPI.GetValue
title: ICodecAPI::GetValue
author: windows-sdk-content
description: The GetValue method gets the current value of a codec property.
old-location: dshow\icodecapi_getvalue.htm
old-project: DirectShow
ms.assetid: 863ba518-c3c6-47d8-96d8-445a7e4d02aa
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetValue, GetValue method [DirectShow], GetValue method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetValue method, ICodecAPI.GetValue, ICodecAPI::GetValue, ICodecAPIGetValue, dshow.icodecapi_getvalue, strmif/ICodecAPI::GetValue
ms.prod: windows
ms.technology: windows-sdk
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
 - ICodecAPI.GetValue
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICodecAPI::GetValue


## -description


The <b>GetValue</b> method gets the current value of a codec property.
      


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="https://msdn.microsoft.com/5d527af7-07cf-42e2-99bb-d56c856cc1bc">Codec API Properties</a>.
          


### -param Value [out]

Pointer to a <b>VARIANT</b> that receives the value of the property. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.
          


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
<dt><b>VFW_E_CODECAPI_NO_CURRENT_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The property does not currently have a value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>



<a href="https://msdn.microsoft.com/e78a310a-3605-4cb3-a0c3-7864c890c1fa">ICodecAPI::SetValue</a>
 

 

