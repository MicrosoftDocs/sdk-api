---
UID: NF:msctf.ITfThreadMgr.CreateDocumentMgr
title: ITfThreadMgr::CreateDocumentMgr
author: windows-sdk-content
description: ITfThreadMgr::CreateDocumentMgr method
old-location: tsf\itfthreadmgr_createdocumentmgr.htm
old-project: TSF
ms.assetid: 0f90a359-61e7-46e5-9d0b-ab6fe24f3136
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: CreateDocumentMgr, CreateDocumentMgr method [Text Services Framework], CreateDocumentMgr method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],CreateDocumentMgr method, ITfThreadMgr.CreateDocumentMgr, ITfThreadMgr::CreateDocumentMgr, _tsf_itfthreadmgr_createdocumentmgr_ref, msctf/ITfThreadMgr::CreateDocumentMgr, tsf.itfthreadmgr_createdocumentmgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfThreadMgr.CreateDocumentMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgr::CreateDocumentMgr


## -description




## -parameters




### -param ppdim [out]

Pointer to an <a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a> interface that receives the document manager object.


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
<i>ppdim</i> is invalid.

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
</table>
 




## -remarks



The caller must release the document manager when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>
 

 

