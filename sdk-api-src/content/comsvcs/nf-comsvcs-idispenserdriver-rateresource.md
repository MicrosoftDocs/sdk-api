---
UID: NF:comsvcs.IDispenserDriver.RateResource
title: IDispenserDriver::RateResource (comsvcs.h)
description: Evaluates how well a candidate resource matches.
helpviewer_keywords: ["IDispenserDriver interface [COM+]","RateResource method","IDispenserDriver.RateResource","IDispenserDriver::RateResource","RateResource","RateResource method [COM+]","RateResource method [COM+]","IDispenserDriver interface","_dtc_IDispenserDriver_RateResource","comsvcs/IDispenserDriver::RateResource","cos.idispenserdriver_rateresource"]
old-location: cos\idispenserdriver_rateresource.htm
tech.root: cos
ms.assetid: 5fe3ca39-e4cb-4dae-be96-ce1a2099486a
ms.date: 12/05/2018
ms.keywords: IDispenserDriver interface [COM+],RateResource method, IDispenserDriver.RateResource, IDispenserDriver::RateResource, RateResource, RateResource method [COM+], RateResource method [COM+],IDispenserDriver interface, _dtc_IDispenserDriver_RateResource, comsvcs/IDispenserDriver::RateResource, cos.idispenserdriver_rateresource
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDispenserDriver::RateResource
 - comsvcs/IDispenserDriver::RateResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IDispenserDriver.RateResource
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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>