---
UID: NF:comsvcs.IDispenserManager.RegisterDispenser
title: IDispenserManager::RegisterDispenser (comsvcs.h)
description: Registers the resource dispenser with the dispenser manager.
helpviewer_keywords: ["IDispenserManager interface [COM+]","RegisterDispenser method","IDispenserManager.RegisterDispenser","IDispenserManager::RegisterDispenser","RegisterDispenser","RegisterDispenser method [COM+]","RegisterDispenser method [COM+]","IDispenserManager interface","_dtc_IDispenserManager_RegisterDispenser","comsvcs/IDispenserManager::RegisterDispenser","cos.idispensermanager_registerdispenser"]
old-location: cos\idispensermanager_registerdispenser.htm
tech.root: cos
ms.assetid: 18633c7f-d589-4e38-82e7-7cdae3fbf1ba
ms.date: 12/05/2018
ms.keywords: IDispenserManager interface [COM+],RegisterDispenser method, IDispenserManager.RegisterDispenser, IDispenserManager::RegisterDispenser, RegisterDispenser, RegisterDispenser method [COM+], RegisterDispenser method [COM+],IDispenserManager interface, _dtc_IDispenserManager_RegisterDispenser, comsvcs/IDispenserManager::RegisterDispenser, cos.idispensermanager_registerdispenser
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
 - IDispenserManager::RegisterDispenser
 - comsvcs/IDispenserManager::RegisterDispenser
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
 - IDispenserManager.RegisterDispenser
---

# IDispenserManager::RegisterDispenser


## -description

Registers the resource dispenser with the dispenser manager.

## -parameters

### -param __MIDL__IDispenserManager0000 [in]

The <a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a> interface the Resource Dispenser offers to the Dispenser Manager to use later to notify the Resource Dispenser.

### -param szDispenserName [in]

A friendly name of the Resource Dispenser for administrator display.

### -param __MIDL__IDispenserManager0001 [out]

The <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iholder">IHolder</a> interface that has been instantiated for the resource dispenser.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

The Resource Dispenser notifies the Dispenser Manager that it has started and is prepared to accept notifications on this <a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a> interface. Then the Dispenser Manager creates the Holder for this new Resource Dispenser and returns it to the Resource Dispenser.



This method does not call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the <i>pDispenserDriver</i> object, but <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iholder-close">IHolder::Close</a> does perform a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on <i>pDispenserDriver</i>. This can cause the Resource Dispenser object to be destroyed prematurely. To prevent this premature destruction, the caller of <b>IDispenserManager::RegisterDispenser</b> must explicitly call <b>AddRef</b> on the <i>pDispenserDriver</i> object.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>