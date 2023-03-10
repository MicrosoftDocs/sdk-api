---
UID: NF:comsvcs.IDispenserDriver.DestroyResource
title: IDispenserDriver::DestroyResource (comsvcs.h)
description: Destroys a resource.
helpviewer_keywords: ["DestroyResource","DestroyResource method [COM+]","DestroyResource method [COM+]","IDispenserDriver interface","IDispenserDriver interface [COM+]","DestroyResource method","IDispenserDriver.DestroyResource","IDispenserDriver::DestroyResource","_dtc_IDispenserDriver_DestroyResource","comsvcs/IDispenserDriver::DestroyResource","cos.idispenserdriver_destroyresource"]
old-location: cos\idispenserdriver_destroyresource.htm
tech.root: cos
ms.assetid: 94e3e340-7dde-4b7f-82a9-83cd2400bde5
ms.date: 12/05/2018
ms.keywords: DestroyResource, DestroyResource method [COM+], DestroyResource method [COM+],IDispenserDriver interface, IDispenserDriver interface [COM+],DestroyResource method, IDispenserDriver.DestroyResource, IDispenserDriver::DestroyResource, _dtc_IDispenserDriver_DestroyResource, comsvcs/IDispenserDriver::DestroyResource, cos.idispenserdriver_destroyresource
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
 - IDispenserDriver::DestroyResource
 - comsvcs/IDispenserDriver::DestroyResource
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
 - IDispenserDriver.DestroyResource
---

# IDispenserDriver::DestroyResource


## -description

Destroys a resource.

## -parameters

### -param ResId [in]

The resource that the Dispenser Manager is asking the Resource Dispenser to destroy.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The Resource Dispenser does not support numeric RESIDs.

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