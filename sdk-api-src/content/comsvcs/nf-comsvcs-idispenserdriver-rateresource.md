---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDispenserDriver::RateResource


## -description


Evaluates how well a candidate resource matches.


## -parameters




### -param ResTypId [in]

The type of resource that the Dispenser Manager is looking to match.


### -param ResId [in]

The candidate resource that the Dispenser Manager is considering.


### -param fRequiresTransactionEnlistment [in]

If <b>TRUE</b>, the candidate resource (<i>ResId</i>), if chosen, requires transaction enlistment. If enlistment is expensive, <b>RateResource</b> might rate such a resource lower than a resource that is already enlisted in the correct transaction.


### -param pRating [out]

The Dispenser's rating of this candidate. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The candidate resource is unusable for this request. The resource is not or cannot be changed to be of type <i>ResTypId</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The candidate is a bad fit, but usable. The Dispenser Manager will continue to suggest candidates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The candidate is better than candidates rated as 1. The Dispenser Manager will continue to suggest candidates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>100</dt>
</dl>
</td>
<td width="60%">
The candidate is a perfect fit. The Dispenser Manager will stop suggesting candidates.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



If <i>fRequiresTransactionEnlistment</i> is <b>FALSE</b>, an object was dispensed this resource in this transaction, the object used and then freed the resource (explicitly or implicitly at end of object lifetime). A second object in the same transaction asks for a similar resource, and the resource that the first object used is considered. This resource is a good candidate because it is already enlisted in the correct transaction.

If a particular type of resource can be used only once per transaction, a resource that has already been used once in the transaction can be identified by an <i>fRequiresTransactionEnlistment</i> of <b>FALSE</b> and can be rejected for further use by returning *<i>pRating</i>=0.




## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>
 

 

