---
UID: NF:textstor.ITextStoreACP2.GetEndACP
title: ITextStoreACP2::GetEndACP
author: windows-sdk-content
description: Gets the number of characters in a document.
old-location: tsf\itextstoreacp2_getendacp.htm
tech.root: TSF
ms.assetid: 61429956-8996-450e-af24-0c91ea974865
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEndACP, GetEndACP method [Text Services Framework], GetEndACP method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetEndACP method, ITextStoreACP2.GetEndACP, ITextStoreACP2::GetEndACP, textstor/ITextStoreACP2::GetEndACP, tsf.itextstoreacp2_getendacp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - ITextStoreACP2.GetEndACP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::GetEndACP


## -description


Gets the number of characters in a document.


## -parameters




### -param pacp [out]

Receives the character position of the last character in the document plus one.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application has not implemented this method. This is usually an indication that calculating the end position requires excessive resources. If the end position is necessary, you can use <a href="https://msdn.microsoft.com/e1443c44-4787-448e-b5ff-a05d1396807d">GetText</a> to calculate it, though this can also be a memory-intensive operation, paging in arbitrarily large amounts of memory from disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e1443c44-4787-448e-b5ff-a05d1396807d">GetText</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>
 

 

