---
UID: NF:msctf.IEnumTfProperties.Next
title: IEnumTfProperties::Next
author: windows-sdk-content
description: IEnumTfProperties::Next method
old-location: tsf\ienumtfproperties_next.htm
old-project: TSF
ms.assetid: a8357166-bfc3-4740-a5b9-91c6c1825ab9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumTfProperties interface [Text Services Framework],Next method, IEnumTfProperties.Next, IEnumTfProperties::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfProperties interface, _tsf_ienumtfproperties_next_ref, msctf/IEnumTfProperties::Next, tsf.ienumtfproperties_next
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfProperties.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfProperties::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param ppProp [out]

Pointer to an array of <a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetched [out]

Pointer to a ULONG that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
<i>ppProp</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/99d8564f-98bc-4f30-bff9-923a4016a5fe">IEnumTfProperties</a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty
      </a>
 

 

