---
UID: NF:tapi3if.IEnumBstr.Clone
title: IEnumBstr::Clone (tapi3if.h)
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages.
old-location: tapi3\ienumbstr_clone.htm
tech.root: Tapi
ms.assetid: 17376fb1-05cc-4ca4-85ab-d578a48f03d1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumBstr interface, IEnumBstr interface [TAPI 2.2],Clone method, IEnumBstr.Clone, IEnumBstr::Clone, _tapi3_ienumbstr_clone, tapi3.ienumbstr_clone, tapi3if/IEnumBstr::Clone
ms.topic: method
f1_keywords: 
 - "tapi3if/IEnumBstr.Clone"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumBstr::Clone


## -description


The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages.


## -parameters




### -param ppEnum [out]

Pointer to new 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr">IEnumBstr</a> interface.


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



TAPI calls the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr">IEnumBstr</a> interface returned by this method. The application must call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method on the 
<b>IEnumBstr</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumagentsession">IEnumAgentSession</a>
 

 

