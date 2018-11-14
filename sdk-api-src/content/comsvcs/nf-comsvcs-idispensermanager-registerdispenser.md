---
UID: NF:comsvcs.IDispenserManager.RegisterDispenser
title: IDispenserManager::RegisterDispenser
author: windows-sdk-content
description: Registers the resource dispenser with the dispenser manager.
old-location: cos\idispensermanager_registerdispenser.htm
tech.root: cossdk
ms.assetid: 18633c7f-d589-4e38-82e7-7cdae3fbf1ba
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDispenserManager interface [COM+],RegisterDispenser method, IDispenserManager.RegisterDispenser, IDispenserManager::RegisterDispenser, RegisterDispenser, RegisterDispenser method [COM+], RegisterDispenser method [COM+],IDispenserManager interface, _dtc_IDispenserManager_RegisterDispenser, comsvcs/IDispenserManager::RegisterDispenser, cos.idispensermanager_registerdispenser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IDispenserManager.RegisterDispenser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IDispenserManager.RegisterDispenser
: 
---

# IDispenserManager::RegisterDispenser


## -description


Registers the resource dispenser with the dispenser manager.


## -parameters




### -param __MIDL__IDispenserManager0000

TBD


### -param szDispenserName [in]

A friendly name of the Resource Dispenser for administrator display.


### -param __MIDL__IDispenserManager0001

TBD




#### - pDispenserDriver [in]

The <a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a> interface the Resource Dispenser offers to the Dispenser Manager to use later to notify the Resource Dispenser.


#### - ppIHolder [out]

The <a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a> interface that has been instantiated for the resource dispenser.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



The Resource Dispenser notifies the Dispenser Manager that it has started and is prepared to accept notifications on this <a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a> interface. Then the Dispenser Manager creates the Holder for this new Resource Dispenser and returns it to the Resource Dispenser.



This method does not call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the <i>pDispenserDriver</i> object, but <a href="https://msdn.microsoft.com/c8aac9b4-04d7-46a7-9b77-5f7d9d6a2ac3">IHolder::Close</a> does perform a <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on <i>pDispenserDriver</i>. This can cause the Resource Dispenser object to be destroyed prematurely. To prevent this premature destruction, the caller of <b>IDispenserManager::RegisterDispenser</b> must explicitly call <b>AddRef</b> on the <i>pDispenserDriver</i> object.





## -see-also




<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>
 

 

