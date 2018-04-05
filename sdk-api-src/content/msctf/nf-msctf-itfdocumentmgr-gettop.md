---
UID: NF:msctf.ITfDocumentMgr.GetTop
title: ITfDocumentMgr::GetTop method
author: windows-driver-content
description: ITfDocumentMgr::GetTop method
old-location: tsf\itfdocumentmgr_gettop.htm
old-project: TSF
ms.assetid: 5be7635f-ec27-4892-9cfe-dba31e202510
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetTop method [Text Services Framework], GetTop method [Text Services Framework], ITfDocumentMgr interface, GetTop,ITfDocumentMgr.GetTop, ITfDocumentMgr, ITfDocumentMgr interface [Text Services Framework], GetTop method, ITfDocumentMgr::GetTop, _tsf_itfdocumentmgr_gettop_ref, msctf/ITfDocumentMgr::GetTop, tsf.itfdocumentmgr_gettop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfDocumentMgr.GetTop
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfDocumentMgr::GetTop method


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



<a href="https://msdn.microsoft.com/71248c77-7440-412c-b565-39c04108b98b">
        ITfDocumentMgr::GetBase
      </a>



<a href="https://msdn.microsoft.com/afd5452b-4121-428d-801f-1638c2767c67">
        ITfDocumentMgr::Push
      </a>
 

 

