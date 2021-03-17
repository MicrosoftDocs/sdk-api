---
UID: NF:comsvcs.IDispenserDriver.CreateResource
title: IDispenserDriver::CreateResource (comsvcs.h)
description: Creates a resource.
helpviewer_keywords: ["CreateResource","CreateResource method [COM+]","CreateResource method [COM+]","IDispenserDriver interface","IDispenserDriver interface [COM+]","CreateResource method","IDispenserDriver.CreateResource","IDispenserDriver::CreateResource","_dtc_IDispenserDriver_CreateResource","comsvcs/IDispenserDriver::CreateResource","cos.idispenserdriver_createresource"]
old-location: cos\idispenserdriver_createresource.htm
tech.root: cos
ms.assetid: 97b49069-3428-48da-a818-737f3bc342d0
ms.date: 12/05/2018
ms.keywords: CreateResource, CreateResource method [COM+], CreateResource method [COM+],IDispenserDriver interface, IDispenserDriver interface [COM+],CreateResource method, IDispenserDriver.CreateResource, IDispenserDriver::CreateResource, _dtc_IDispenserDriver_CreateResource, comsvcs/IDispenserDriver::CreateResource, cos.idispenserdriver_createresource
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
 - IDispenserDriver::CreateResource
 - comsvcs/IDispenserDriver::CreateResource
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
 - IDispenserDriver.CreateResource
---

# IDispenserDriver::CreateResource


## -description

Creates a resource.

## -parameters

### -param ResTypId [in]

The type of resource to be created.

### -param pResId [out]

A handle to the newly created resource.

### -param pSecsFreeBeforeDestroy [out]

The time-out of the new resource. This is the number of seconds that this resource is allowed to remain idle in the pool before it is destroyed.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

The <b>CreateResource</b> method is called by the Dispenser Manager in the following cases:

<ul>
<li>When a resource is needed and there is no inventory to satisfy an <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iholder-allocresource">IHolder::AllocResource</a> call when none were found in inventory.</li>
<li>When the Dispenser Manager is setting up initial inventory.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>