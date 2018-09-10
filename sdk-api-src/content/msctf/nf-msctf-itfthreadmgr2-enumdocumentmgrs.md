---
UID: NF:msctf.ITfThreadMgr2.EnumDocumentMgrs
title: ITfThreadMgr2::EnumDocumentMgrs
author: windows-sdk-content
description: Returns an enumerator for all the document managers within the calling thread.
old-location: tsf\itfthreadmgr2_enumdocumentmgrs.htm
tech.root: TSF
ms.assetid: 16A07BA6-05C2-4CA6-97D6-F1B4CEE1E757
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumDocumentMgrs, EnumDocumentMgrs method [Text Services Framework], EnumDocumentMgrs method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],EnumDocumentMgrs method, ITfThreadMgr2.EnumDocumentMgrs, ITfThreadMgr2::EnumDocumentMgrs, msctf/ITfThreadMgr2::EnumDocumentMgrs, tsf.itfthreadmgr2_enumdocumentmgrs
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.EnumDocumentMgrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfThreadMgr2::EnumDocumentMgrs


## -description


Returns an enumerator for all the document managers within the calling thread.


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




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

