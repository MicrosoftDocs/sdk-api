---
UID: NF:tapi3if.ITBasicCallControl.Answer
title: ITBasicCallControl::Answer
author: windows-driver-content
description: The Answer method answers an incoming call. This method can succeed only if the call state is CS_OFFERING.
old-location: tapi3\itbasiccallcontrol_answer.htm
old-project: Tapi
ms.assetid: 81928cf7-082e-44e1-a631-a50a1f01ecec
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: Answer, Answer method [TAPI 2.2], Answer method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Answer method, ITBasicCallControl.Answer, ITBasicCallControl::Answer, _tapi3_itbasiccallcontrol_answer, tapi3.itbasiccallcontrol_answer, tapi3if/ITBasicCallControl::Answer
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITBasicCallControl.Answer
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicCallControl::Answer


## -description


The 
<b>Answer</b> method answers an incoming call. This method can succeed only if the 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a> is CS_OFFERING.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Call state was not CS_OFFERING.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/34ac0b34-1d1b-4657-a737-27a4ed9326af">Answer Overview</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/dd51991c-c044-4b88-8f97-9e0ae701a2a5">lineAnswer</a>
 

 

