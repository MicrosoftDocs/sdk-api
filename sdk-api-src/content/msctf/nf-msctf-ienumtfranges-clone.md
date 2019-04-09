---
UID: NF:msctf.IEnumTfRanges.Clone
title: IEnumTfRanges::Clone (msctf.h)
author: windows-sdk-content
description: IEnumTfRanges::Clone method
old-location: tsf\ienumtfranges_clone.htm
tech.root: TSF
ms.assetid: 5e51a747-0b77-4ba3-b03c-217a3f81a0aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfRanges interface, IEnumTfRanges interface [Text Services Framework],Clone method, IEnumTfRanges.Clone, IEnumTfRanges::Clone, _tsf_ienumtfranges_clone_ref, msctf/IEnumTfRanges::Clone, tsf.ienumtfranges_clone
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
 - IEnumTfRanges.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfRanges::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/68e17539-3b00-4e51-964d-0516b448f6c8">IEnumTfRanges</a> interface pointer that receives the new enumerator.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/68e17539-3b00-4e51-964d-0516b448f6c8">IEnumTfRanges
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

