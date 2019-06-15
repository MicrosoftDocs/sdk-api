---
UID: NF:msctf.ITfContext.EnumProperties
title: ITfContext::EnumProperties (msctf.h)
author: windows-sdk-content
description: ITfContext::EnumProperties method
old-location: tsf\itfcontext_enumproperties.htm
tech.root: TSF
ms.assetid: b57c9fdc-320b-4d97-8af4-c75756326437
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumProperties, EnumProperties method [Text Services Framework], EnumProperties method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],EnumProperties method, ITfContext.EnumProperties, ITfContext::EnumProperties, _tsf_itfcontext_enumproperties_ref, msctf/ITfContext::EnumProperties, tsf.itfcontext_enumproperties
ms.topic: method
f1_keywords: ["msctf/ITfContext.EnumProperties"]
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
ms.custom: 19H1
---

# ITfContext::EnumProperties


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumtfproperties">IEnumTfProperties</a> interface pointer that receives the enumerator object.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumtfproperties">IEnumTfProperties
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a>
 

 

