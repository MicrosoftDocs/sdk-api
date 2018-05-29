---
UID: NF:objidl.IEnumSTATSTG.Clone
title: IEnumSTATSTG::Clone
author: windows-sdk-content
description: Creates a new enumerator that contains the same enumeration state as the current STATSTG structure enumerator.
old-location: stg\ienumstatstg_clone.htm
old-project: Stg
ms.assetid: b6bc5dbd-7e09-4590-a7d4-d58fcd297f74
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IEnumSTATSTG interface, IEnumSTATSTG interface [Structured Storage],Clone method, IEnumSTATSTG.Clone, IEnumSTATSTG::Clone, objidl/IEnumSTATSTG::Clone, stg.ienumstatstg_clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IEnumSTATSTG.Clone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSTATSTG::Clone


## -description


The <b>Clone</b> method creates a new enumerator that contains the same enumeration state as the current <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure enumerator. Using this method, a client can record a particular point in the enumeration sequence and then return to that point at a later time. The new enumerator supports the same <a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a> interface.


## -parameters




### -param ppenum [out]

    A pointer to the variable that receives the  <a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a> interface pointer. 

If the method is unsuccessful, the value of the <i>ppenum</i> parameter is undefined.


## -returns



This method supports the following return values.

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
The <i>ppenum</i> parameter is <b>NULL</b>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception occurred.

</td>
</tr>
</table>
 



