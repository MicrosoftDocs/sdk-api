---
UID: NF:tapi3.IEnumAgent.Reset
title: IEnumAgent::Reset
author: windows-sdk-content
description: The Reset method resets the enumeration sequence to the beginning.
old-location: tapi3\ienumagent_reset.htm
old-project: Tapi
ms.assetid: e909135a-04ed-4602-991e-915744667df7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IEnumAgent interface [TAPI 2.2],Reset method, IEnumAgent.Reset, IEnumAgent::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumAgent interface, _tapi3_ienumagent_reset, tapi3.ienumagent_reset, tapi3cc/IEnumAgent::Reset
ms.prod: windows
ms.technology: windows-sdk
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
-	IEnumAgent.Reset
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAgent::Reset


## -description


The 
<b>Reset</b> method resets the enumeration sequence to the beginning.


## -parameters






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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4c75314c-72f0-4eae-a1f5-36f3959c322a">IEnumAgent</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>
 

 

