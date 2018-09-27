---
UID: NF:msctf.IEnumTfDocumentMgrs.Clone
title: IEnumTfDocumentMgrs::Clone
author: windows-sdk-content
description: IEnumTfDocumentMgrs::Clone method
old-location: tsf\ienumtfdocumentmgrs_clone.htm
tech.root: TSF
ms.assetid: d7a6ff9c-327b-45bf-93d0-7bf08065ad9c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfDocumentMgrs interface, IEnumTfDocumentMgrs interface [Text Services Framework],Clone method, IEnumTfDocumentMgrs.Clone, IEnumTfDocumentMgrs::Clone, _tsf_ienumtfdocumentmgrs_clone_ref, msctf/IEnumTfDocumentMgrs::Clone, tsf.ienumtfdocumentmgrs_clone
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
 - IEnumTfDocumentMgrs.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfDocumentMgrs::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/5b276752-715b-4426-ad37-8658bae4c1a6">IEnumTfDocumentMgrs</a> interface pointer that receives the new enumerator.


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




<a href="https://msdn.microsoft.com/5b276752-715b-4426-ad37-8658bae4c1a6">IEnumTfDocumentMgrs
      </a>
 

 

