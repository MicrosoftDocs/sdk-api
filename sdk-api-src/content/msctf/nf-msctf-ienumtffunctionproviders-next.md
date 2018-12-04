---
UID: NF:msctf.IEnumTfFunctionProviders.Next
title: IEnumTfFunctionProviders::Next
author: windows-sdk-content
description: IEnumTfFunctionProviders::Next method
old-location: tsf\ienumtffunctionproviders_next.htm
tech.root: TSF
ms.assetid: c9938eb0-c084-4663-9aef-584c987a08a7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IEnumTfFunctionProviders interface [Text Services Framework],Next method, IEnumTfFunctionProviders.Next, IEnumTfFunctionProviders::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfFunctionProviders interface, _tsf_ienumtffunctionproviders_next_ref, msctf/IEnumTfFunctionProviders::Next, tsf.ienumtffunctionproviders_next
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
 - IEnumTfFunctionProviders.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfFunctionProviders::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param ppCmdobj [out]

Pointer to an array of <a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetch [out]

Pointer to a ULONG value that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
<i>ppCmdobj</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/21e2f1c8-926e-4e53-b8d1-aecc2d1a97cb">IEnumTfFunctionProviders</a>



<a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider
      </a>
 

 

