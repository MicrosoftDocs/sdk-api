---
UID: NF:strmif.ICodecAPI.GetDefaultValue
title: ICodecAPI::GetDefaultValue
author: windows-driver-content
description: The GetDefaultValue method gets the default value of a codec property.
old-location: dshow\icodecapi_getdefaultvalue.htm
old-project: DirectShow
ms.assetid: 749f5235-2f62-4609-84b8-a880a38cd9cb
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetDefaultValue, GetDefaultValue method [DirectShow], GetDefaultValue method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetDefaultValue method, ICodecAPI.GetDefaultValue, ICodecAPI::GetDefaultValue, ICodecAPIGetDefaultValue, dshow.icodecapi_getdefaultvalue, strmif/ICodecAPI::GetDefaultValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	ICodecAPI.GetDefaultValue
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICodecAPI::GetDefaultValue


## -description



        The <b>GetDefaultValue</b> method gets the default value of a codec property.
      


## -parameters




### -param Api [in]


            Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="https://msdn.microsoft.com/5d527af7-07cf-42e2-99bb-d56c856cc1bc">Codec API Properties</a>.
          


### -param Value [out]


            Pointer to a <b>VARIANT</b> that receives the default value. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.
          


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
<dt><b>VFW_E_CODECAPI_NO_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The specified property does not have a default value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>
 

 

