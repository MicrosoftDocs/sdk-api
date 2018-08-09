---
UID: NF:msctf.ITfThreadMgr2.CreateDocumentMgr
title: ITfThreadMgr2::CreateDocumentMgr
author: windows-sdk-content
description: Creates a document manager object.
old-location: tsf\itfthreadmgr2_createdocumentmgr.htm
old-project: TSF
ms.assetid: 4B19EA80-9F42-4FFF-AB3D-4D0B5B2174F8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateDocumentMgr, CreateDocumentMgr method [Text Services Framework], CreateDocumentMgr method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],CreateDocumentMgr method, ITfThreadMgr2.CreateDocumentMgr, ITfThreadMgr2::CreateDocumentMgr, msctf/ITfThreadMgr2::CreateDocumentMgr, tsf.itfthreadmgr2_createdocumentmgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - msctf.h
api_name:
 - ITfThreadMgr2.CreateDocumentMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgr2::CreateDocumentMgr


## -description


Creates a document manager object.


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




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

