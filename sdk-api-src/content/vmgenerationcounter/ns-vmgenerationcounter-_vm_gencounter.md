---
UID: NS:vmgenerationcounter._VM_GENCOUNTER
title: "_VM_GENCOUNTER"
author: windows-sdk-content
description: Describes a virtual machine generation identifier.
old-location: hyperv\vm_gencounter.htm
tech.root: HyperV_v2
ms.assetid: F1F2C867-2607-40AD-92B7-E7C07304D885
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PVM_GENCOUNTER, PVM_GENCOUNTER, PVM_GENCOUNTER structure pointer, VM_GENCOUNTER, VM_GENCOUNTER structure, _VM_GENCOUNTER, hyperv.vm_gencounter, vmgenerationcounter/PVM_GENCOUNTER, vmgenerationcounter/VM_GENCOUNTER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vmgenerationcounter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - Vmgenerationcounter.h
api_name:
 - VM_GENCOUNTER
product: Windows
targetos: Windows
req.typenames: VM_GENCOUNTER, *PVM_GENCOUNTER
req.redist: 
---

# _VM_GENCOUNTER structure


## -description


Describes a virtual machine generation identifier.


## -struct-fields




### -field GenerationCount

The low 64 bits of the virtual machine generation identifier. 


### -field GenerationCountHigh

The high 64 bits of the virtual machine generation identifier. 


## -remarks



For info about the virtual machine generation identifier, see <a href="https://msdn.microsoft.com/0793E46B-8464-425E-8C5B-77C14DA90004">Virtual machine generation identifier</a>.




## -see-also




<a href="https://msdn.microsoft.com/D8945F17-8982-4694-BDD9-DD67963626D1">IOCTL_VMGENCOUNTER_READ</a>
 

 

