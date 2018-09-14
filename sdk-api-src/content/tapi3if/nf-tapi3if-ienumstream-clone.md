---
UID: NF:tapi3if.IEnumStream.Clone
title: IEnumStream::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: tapi3\ienumstream_clone.htm
tech.root: TAPI
ms.assetid: fbb29d36-b93a-44e2-a1df-74b6de6f4e6e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumStream interface, IEnumStream interface [TAPI 2.2],Clone method, IEnumStream.Clone, IEnumStream::Clone, _tapi3_ienumstream_clone, tapi3.ienumstream_clone, tapi3if/IEnumStream::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - tapi3if.h
api_name:
 - IEnumStream.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumStream::Clone


## -description


The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to new 
<a href="https://msdn.microsoft.com/52e8c040-8bc5-4c9c-a697-ec05164adea2">IEnumStream</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/52e8c040-8bc5-4c9c-a697-ec05164adea2">IEnumStream</a> interface returned by <b>IEnumStream::Clone</b>. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>IEnumStream</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/52e8c040-8bc5-4c9c-a697-ec05164adea2">IEnumStream</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

