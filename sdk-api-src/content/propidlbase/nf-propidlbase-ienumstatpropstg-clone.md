---
UID: NF:propidlbase.IEnumSTATPROPSTG.Clone
title: IEnumSTATPROPSTG::Clone
author: windows-sdk-content
description: Creates an enumerator that contains the same enumeration state as the current STATPROPSTG structure enumerator.
old-location: stg\ienumstatpropstg_clone.htm
old-project: stg
ms.assetid: e06e109a-3f9d-4b08-bde9-888cb795287c
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IEnumSTATPROPSTG interface, IEnumSTATPROPSTG interface [Structured Storage],Clone method, IEnumSTATPROPSTG.Clone, IEnumSTATPROPSTG::Clone, propidlbase/IEnumSTATPROPSTG::Clone, stg.ienumstatpropstg_clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STATPROPSTG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATPROPSTG.Clone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IEnumSTATPROPSTG::Clone


## -description


The <b>Clone</b> method creates an enumerator that contains the same enumeration state as the current <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structure enumerator. Using this method, a client can record a particular point in the enumeration sequence and then return to that point later. The new enumerator supports the same <a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a> interface.


## -parameters




### -param ppenum [out]

    A pointer to the variable that receives the  <a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a> interface pointer. 

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
 



