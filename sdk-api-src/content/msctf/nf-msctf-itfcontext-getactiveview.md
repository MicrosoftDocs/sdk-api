---
UID: NF:msctf.ITfContext.GetActiveView
title: ITfContext::GetActiveView
author: windows-sdk-content
description: ITfContext::GetActiveView method
old-location: tsf\itfcontext_getactiveview.htm
tech.root: TSF
ms.assetid: 41f7eb74-bca2-4d53-8a70-0b872616fd1b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetActiveView, GetActiveView method [Text Services Framework], GetActiveView method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetActiveView method, ITfContext.GetActiveView, ITfContext::GetActiveView, _tsf_itfcontext_getactiveview_ref, msctf/ITfContext::GetActiveView, tsf.itfcontext_getactiveview
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
 - ITfContext.GetActiveView
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfContext.GetActiveView
: 
---

# ITfContext::GetActiveView


## -description




## -parameters




### -param ppView [out]

Pointer to an <a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView</a> interface pointer that receives a reference to the active view.


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
The context is not on a document stack.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>



<a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView
      </a>
 

 

