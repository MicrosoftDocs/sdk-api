---
UID: NF:textstor.ITextStoreAnchor.GetEnd
title: ITextStoreAnchor::GetEnd
author: windows-sdk-content
description: The ITextStoreAnchor::GetEnd method returns an anchor positioned at the end of the text stream.
old-location: tsf\itextstoreanchor_getend.htm
tech.root: TSF
ms.assetid: 4c510900-bcff-4ea1-a8f3-95b6f47b3432
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnd, GetEnd method [Text Services Framework], GetEnd method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetEnd method, ITextStoreAnchor.GetEnd, ITextStoreAnchor::GetEnd, textstor/ITextStoreAnchor::GetEnd, tsf.itextstoreanchor_getend
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITextStoreAnchor.GetEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor::GetEnd


## -description


The <b>ITextStoreAnchor::GetEnd</b> method returns an anchor positioned at the end of the text stream.


## -parameters




### -param ppaEnd [out]

Pointer to an anchor object located at the very end of the text stream.


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
<i>ppaEnd</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application has not implemented this method. This is usually an indication that calculating the end position requires excessive resources. If the end position is necessary, you can use <a href="https://msdn.microsoft.com/fd3f91df-b107-4284-8435-d859c843555f">ITextStoreAnchor::GetText</a> to calculate it, though this might also be a memory-intensive operation, paging in arbitrarily large amounts of memory from disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The attempt to instantiate an anchor at the end of the document failed.

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




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/fd3f91df-b107-4284-8435-d859c843555f">ITextStoreAnchor::GetText
      </a>
 

 

