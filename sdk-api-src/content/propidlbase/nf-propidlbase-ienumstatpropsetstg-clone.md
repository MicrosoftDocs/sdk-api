---
UID: NF:propidlbase.IEnumSTATPROPSETSTG.Clone
title: IEnumSTATPROPSETSTG::Clone
author: windows-sdk-content
description: Creates an enumerator that contains the same enumeration state as the current STATPROPSETSTG structure enumerator.
old-location: stg\ienumstatpropsetstg_clone.htm
old-project: Stg
ms.assetid: f875d5e9-fac0-4961-9570-342f55cf307e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IEnumSTATPROPSETSTG interface, IEnumSTATPROPSETSTG interface [Structured Storage],Clone method, IEnumSTATPROPSETSTG.Clone, IEnumSTATPROPSETSTG::Clone, propidlbase/IEnumSTATPROPSETSTG::Clone, stg.ienumstatpropsetstg_clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STATPROPSTG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IEnumSTATPROPSETSTG.Clone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSTATPROPSETSTG::Clone


## -description


The <b>Clone</b> method creates an enumerator that contains the same enumeration state as the current <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structure enumerator. Using this method, a client can record a particular point in the enumeration sequence and then return to that point later. The new enumerator supports the same <a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a> interface.


## -parameters




### -param ppenum [out]

    A pointer to the variable that receives the  <a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a> interface pointer. 

If the method does not succeed, the value of the <i>ppenum</i> parameter is undefined.


## -returns



This method supports return values listed in the following table.

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
 



