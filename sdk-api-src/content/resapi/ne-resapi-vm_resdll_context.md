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

# VM_RESDLL_CONTEXT enumeration


## -description


Contains actions for a virtual machine to perform.


## -enum-fields




### -field VmResdllContextTurnOff

Turns off the virtual machine.


### -field VmResdllContextSave

Saves the virtual machine.


### -field VmResdllContextShutdown

Shuts down the virtual machine.


### -field VmResdllContextShutdownForce

Forces a shutdown of the virtual machine.


### -field VmResdllContextLiveMigration

Performs a live migration of the virtual machine.


## -remarks



The values in this enumeration can be used in a 
    <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> as input for the 
    <a href="https://msdn.microsoft.com/CE56BA9D-3527-43D3-8656-EA0BBDF48B98">MoveClusterGroupEx</a> function's 
    <i>lpInBuffer</i> parameter to specify actions to take on a virtual machine. The resource type 
    name to use in the <a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a> 
    structure is "Virtual Machine" or "Virtual Machine Configuration", and the 
    proper <a href="https://msdn.microsoft.com/a5e06aaf-96ef-41e9-ab73-c0edc8f34d12">CLUSTER_PROPERTY_FORMAT</a> enumeration value to 
    specify for the data format is <b>CLUSPROP_FORMAT_DWORD</b>.




## -see-also




<a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a>



<a href="https://msdn.microsoft.com/a5e06aaf-96ef-41e9-ab73-c0edc8f34d12">CLUSTER_PROPERTY_FORMAT</a>



<a href="https://msdn.microsoft.com/CE56BA9D-3527-43D3-8656-EA0BBDF48B98">MoveClusterGroupEx</a>



<a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">Property Lists</a>
 

 

