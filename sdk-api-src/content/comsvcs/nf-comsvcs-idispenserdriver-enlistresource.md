---
UID: NF:comsvcs.IDispenserDriver.EnlistResource
title: IDispenserDriver::EnlistResource (comsvcs.h)
description: Enlists a resource in a transaction.
helpviewer_keywords: ["EnlistResource","EnlistResource method [COM+]","EnlistResource method [COM+]","IDispenserDriver interface","IDispenserDriver interface [COM+]","EnlistResource method","IDispenserDriver.EnlistResource","IDispenserDriver::EnlistResource","_dtc_IDispenserDriver_EnlistResource","comsvcs/IDispenserDriver::EnlistResource","cos.idispenserdriver_enlistresource"]
old-location: cos\idispenserdriver_enlistresource.htm
tech.root: cos
ms.assetid: 87a8b7f4-edf3-4ab5-b75a-f8fda1f4975a
ms.date: 12/05/2018
ms.keywords: EnlistResource, EnlistResource method [COM+], EnlistResource method [COM+],IDispenserDriver interface, IDispenserDriver interface [COM+],EnlistResource method, IDispenserDriver.EnlistResource, IDispenserDriver::EnlistResource, _dtc_IDispenserDriver_EnlistResource, comsvcs/IDispenserDriver::EnlistResource, cos.idispenserdriver_enlistresource
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
 - IDispenserDriver::EnlistResource
 - comsvcs/IDispenserDriver::EnlistResource
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
 - IDispenserDriver.EnlistResource
---

# IDispenserDriver::EnlistResource


## -description

Enlists a resource in a transaction.

## -parameters

### -param ResId [in]

The resource that the Dispenser Manager is asking to be enlisted in transaction <i>TransId</i>.

### -param TransId [in]

The transaction that the Dispenser Manager wants the Resource Dispenser to enlist resource <i>ResId</i> in. The Dispenser Manager passes 0 to indicate that the Resource Dispenser should ensure that the resource is not enlisted in any transaction.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The resource is not enlistable (not transaction capable).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

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

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>