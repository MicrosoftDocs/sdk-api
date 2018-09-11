---
UID: NF:tapi3if.IEnumBstr.Clone
title: IEnumBstr::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages.
old-location: tapi3\ienumbstr_clone.htm
tech.root: tapi
ms.assetid: 17376fb1-05cc-4ca4-85ab-d578a48f03d1
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumBstr interface, IEnumBstr interface [TAPI 2.2],Clone method, IEnumBstr.Clone, IEnumBstr::Clone, _tapi3_ienumbstr_clone, tapi3.ienumbstr_clone, tapi3if/IEnumBstr::Clone
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumBstr.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBstr::Clone


## -description


The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages.


## -parameters




### -param ppEnum [out]

Pointer to new 
<a href="https://msdn.microsoft.com/0e87ec06-7f3a-410c-9d54-7a67991e089c">IEnumBstr</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<a href="https://msdn.microsoft.com/0e87ec06-7f3a-410c-9d54-7a67991e089c">IEnumBstr</a> interface returned by this method. The application must call the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> method on the 
<b>IEnumBstr</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/38b9fc57-a0af-4dfa-9058-e721138c8be9">IEnumAgentSession</a>
 

 

