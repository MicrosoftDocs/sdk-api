---
UID: NF:msctf.ITfContext.EnumProperties
title: ITfContext::EnumProperties
author: windows-sdk-content
description: ITfContext::EnumProperties method
old-location: tsf\itfcontext_enumproperties.htm
tech.root: TSF
ms.assetid: b57c9fdc-320b-4d97-8af4-c75756326437
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EnumProperties, EnumProperties method [Text Services Framework], EnumProperties method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],EnumProperties method, ITfContext.EnumProperties, ITfContext::EnumProperties, _tsf_itfcontext_enumproperties_ref, msctf/ITfContext::EnumProperties, tsf.itfcontext_enumproperties
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
 - ITfContext.EnumProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContext::EnumProperties


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/99d8564f-98bc-4f30-bff9-923a4016a5fe">IEnumTfProperties</a> interface pointer that receives the enumerator object.


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
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEnum</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/99d8564f-98bc-4f30-bff9-923a4016a5fe">IEnumTfProperties
      </a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>
 

 

