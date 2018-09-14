---
UID: NF:msctf.ITfDocumentMgr.GetBase
title: ITfDocumentMgr::GetBase
author: windows-sdk-content
description: ITfDocumentMgr::GetBase method
old-location: tsf\itfdocumentmgr_getbase.htm
tech.root: TSF
ms.assetid: 71248c77-7440-412c-b565-39c04108b98b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetBase, GetBase method [Text Services Framework], GetBase method [Text Services Framework],ITfDocumentMgr interface, ITfDocumentMgr interface [Text Services Framework],GetBase method, ITfDocumentMgr.GetBase, ITfDocumentMgr::GetBase, _tsf_itfdocumentmgr_getbase_ref, msctf/ITfDocumentMgr::GetBase, tsf.itfdocumentmgr_getbase
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
 - ITfDocumentMgr.GetBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfDocumentMgr::GetBase


## -description




## -parameters




### -param ppic [out]

Address of an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> pointer that receives the context.


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
<i>ppic</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a>



<a href="https://msdn.microsoft.com/5be7635f-ec27-4892-9cfe-dba31e202510">ITfDocumentMgr::GetTop
      </a>



<a href="https://msdn.microsoft.com/afd5452b-4121-428d-801f-1638c2767c67">ITfDocumentMgr::Push
      </a>
 

 

