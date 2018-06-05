---
UID: NF:msctf.ITfThreadMgr.EnumDocumentMgrs
title: ITfThreadMgr::EnumDocumentMgrs
author: windows-sdk-content
description: ITfThreadMgr::EnumDocumentMgrs method
old-location: tsf\itfthreadmgr_enumdocumentmgrs.htm
old-project: TSF
ms.assetid: 0b6f61fb-0ca0-4b93-ad30-d1e080b9bde1
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: EnumDocumentMgrs, EnumDocumentMgrs method [Text Services Framework], EnumDocumentMgrs method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],EnumDocumentMgrs method, ITfThreadMgr.EnumDocumentMgrs, ITfThreadMgr::EnumDocumentMgrs, _tsf_itfthreadmgr_enumdocumentmgrs_ref, msctf/ITfThreadMgr::EnumDocumentMgrs, tsf.itfthreadmgr_enumdocumentmgrs
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
-	ITfThreadMgr.EnumDocumentMgrs
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgr::EnumDocumentMgrs


## -description




## -parameters




### -param ppEnum [out]

Pointer to a <a href="https://msdn.microsoft.com/5b276752-715b-4426-ad37-8658bae4c1a6">IEnumTfDocumentMgrs</a> interface that receives the enumerator.


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
<i>ppEnum</i> is invalid.

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
 




## -remarks



The caller must release the enumerator when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/5b276752-715b-4426-ad37-8658bae4c1a6">IEnumTfDocumentMgrs
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>
 

 

