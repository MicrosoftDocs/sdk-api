---
UID: NF:tapi3.IEnumAgent.Clone
title: IEnumAgent::Clone method
author: windows-driver-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: tapi3\ienumagent_clone.htm
old-project: Tapi
ms.assetid: e6e23f6b-a91a-43c1-8e37-f37d7284cef6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: Clone method [TAPI 2.2], Clone method [TAPI 2.2], IEnumAgent interface, Clone,IEnumAgent.Clone, IEnumAgent, IEnumAgent interface [TAPI 2.2], Clone method, IEnumAgent::Clone, _tapi3_ienumagent_clone, tapi3.ienumagent_clone, tapi3cc/IEnumAgent::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3.h
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
req.typenames: MSP_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	IEnumAgent.Clone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAgent::Clone method


## -description


The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to new 
<a href="https://msdn.microsoft.com/4c75314c-72f0-4eae-a1f5-36f3959c322a">IEnumAgent</a> interface.


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



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/4c75314c-72f0-4eae-a1f5-36f3959c322a">IEnumAgent</a> interface returned by <b>IEnumAgent::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumAgent</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/4c75314c-72f0-4eae-a1f5-36f3959c322a">IEnumAgent</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>
 

 

