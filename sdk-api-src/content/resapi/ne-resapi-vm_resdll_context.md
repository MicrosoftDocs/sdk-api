---
UID: NE:resapi.VM_RESDLL_CONTEXT
title: VM_RESDLL_CONTEXT
author: windows-sdk-content
description: Contains actions for a virtual machine to perform.
old-location: mscs\vm_resdll_context.htm
tech.root: mscs
ms.assetid: F01306D5-9D46-4489-AB38-67029EEFE6D0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PVM_RESDLL_CONTEXT, PVM_RESDLL_CONTEXT, PVM_RESDLL_CONTEXT enumeration pointer [Failover Cluster], VM_RESDLL_CONTEXT, VM_RESDLL_CONTEXT enumeration [Failover Cluster], VmResdllContextLiveMigration, VmResdllContextSave, VmResdllContextShutdown, VmResdllContextShutdownForce, VmResdllContextTurnOff, mscs.vm_resdll_context, resapi/PVM_RESDLL_CONTEXT, resapi/VM_RESDLL_CONTEXT, resapi/VmResdllContextLiveMigration, resapi/VmResdllContextSave, resapi/VmResdllContextShutdown, resapi/VmResdllContextShutdownForce, resapi/VmResdllContextTurnOff"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - VM_RESDLL_CONTEXT
product: Windows
targetos: Windows
req.typenames: VM_RESDLL_CONTEXT, *PVM_RESDLL_CONTEXT
req.redist: 
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
 

 

