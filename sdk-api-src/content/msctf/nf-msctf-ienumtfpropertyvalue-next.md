---
UID: NF:msctf.IEnumTfPropertyValue.Next
title: IEnumTfPropertyValue::Next
author: windows-sdk-content
description: IEnumTfPropertyValue::Next method
old-location: tsf\ienumtfpropertyvalue_next.htm
tech.root: TSF
ms.assetid: b0fe154c-df33-443d-95a2-f41e7b02def8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEnumTfPropertyValue interface [Text Services Framework],Next method, IEnumTfPropertyValue.Next, IEnumTfPropertyValue::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfPropertyValue interface, _tsf_ienumtfpropertyvalue_next_ref, msctf/IEnumTfPropertyValue::Next, tsf.ienumtfpropertyvalue_next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfPropertyValue.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfPropertyValue::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param rgValues [out]

Pointer to an array of <a href="https://msdn.microsoft.com/50a5930c-ba17-4441-99a7-efc6c4bfc2ab">TF_PROPERTYVAL</a> structures that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>rgValues</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7f99df15-777c-46eb-bff3-542eb1fcc428">IEnumTfPropertyValue</a>



<a href="https://msdn.microsoft.com/50a5930c-ba17-4441-99a7-efc6c4bfc2ab">TF_PROPERTYVAL
      </a>
 

 

