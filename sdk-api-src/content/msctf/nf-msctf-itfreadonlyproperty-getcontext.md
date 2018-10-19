---
UID: NF:msctf.ITfReadOnlyProperty.GetContext
title: ITfReadOnlyProperty::GetContext
author: windows-sdk-content
description: ITfReadOnlyProperty::GetContext method
old-location: tsf\itfreadonlyproperty_getcontext.htm
tech.root: TSF
ms.assetid: 2f6becd7-c4d0-45ed-8038-1f706d8e60c7
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetContext, GetContext method [Text Services Framework], GetContext method [Text Services Framework],ITfReadOnlyProperty interface, ITfReadOnlyProperty interface [Text Services Framework],GetContext method, ITfReadOnlyProperty.GetContext, ITfReadOnlyProperty::GetContext, _tsf_itfreadonlyproperty_getcontext_ref, msctf/ITfReadOnlyProperty::GetContext, tsf.itfreadonlyproperty_getcontext
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
 - ITfReadOnlyProperty.GetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfReadOnlyProperty::GetContext


## -description




## -parameters




### -param ppContext [out]

Pointer to an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface pointer that receives the context object. The caller must release this object when it is no longer required.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppContext</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">ITfReadOnlyProperty</a>
 

 

