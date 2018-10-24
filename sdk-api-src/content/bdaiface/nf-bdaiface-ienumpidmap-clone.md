---
UID: NF:bdaiface.IEnumPIDMap.Clone
title: IEnumPIDMap::Clone
author: windows-sdk-content
description: The Clone method creates a copy the collection.
old-location: dshow\ienumpidmap_clone.htm
tech.root: DirectShow
ms.assetid: 4d965a71-ff5e-4d4a-8976-0de5b8bbae04
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumPIDMap interface, IEnumPIDMap interface [DirectShow],Clone method, IEnumPIDMap.Clone, IEnumPIDMap::Clone, IEnumPIDMapClone, bdaiface/IEnumPIDMap::Clone, dshow.ienumpidmap_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEnumPIDMap.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPIDMap::Clone


## -description



The <code>Clone</code> method creates a copy the collection.




## -parameters




### -param ppIEnumPIDMap [out]

Receives an <a href="https://msdn.microsoft.com/d46010c4-0f16-4c97-ad10-16f7ac250390">IEnumPIDMap</a> interface pointer, representing the new collection. The caller must release the interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>ppIEnumPIDMap</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



The caller must release the returned <b>IEnumPIDMap</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d46010c4-0f16-4c97-ad10-16f7ac250390">IEnumPIDMap Interface</a>
 

 

