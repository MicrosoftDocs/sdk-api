---
UID: NF:comsvcs.IDispenserDriver.ResetResource
title: IDispenserDriver::ResetResource (comsvcs.h)
description: Prepares the resource to be put back into general or enlisted inventory.
helpviewer_keywords: ["IDispenserDriver interface [COM+]","ResetResource method","IDispenserDriver.ResetResource","IDispenserDriver::ResetResource","ResetResource","ResetResource method [COM+]","ResetResource method [COM+]","IDispenserDriver interface","_dtc_IDispenserDriver_ResetResource","comsvcs/IDispenserDriver::ResetResource","cos.idispenserdriver_resetresource"]
old-location: cos\idispenserdriver_resetresource.htm
tech.root: cos
ms.assetid: 59df0703-90ea-480c-8608-7d43039b48ba
ms.date: 12/05/2018
ms.keywords: IDispenserDriver interface [COM+],ResetResource method, IDispenserDriver.ResetResource, IDispenserDriver::ResetResource, ResetResource, ResetResource method [COM+], ResetResource method [COM+],IDispenserDriver interface, _dtc_IDispenserDriver_ResetResource, comsvcs/IDispenserDriver::ResetResource, cos.idispenserdriver_resetresource
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
 - IDispenserDriver::ResetResource
 - comsvcs/IDispenserDriver::ResetResource
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
 - IDispenserDriver.ResetResource
---

# IDispenserDriver::ResetResource


## -description

Prepares the resource to be put back into general or enlisted inventory.

## -parameters

### -param ResId [in]

The resource to be reset.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ResId</i> is not a valid resource handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -remarks

The resource may still be enlisted at this time, so <b>ResetResource</b> cannot disrupt the enlistment.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>