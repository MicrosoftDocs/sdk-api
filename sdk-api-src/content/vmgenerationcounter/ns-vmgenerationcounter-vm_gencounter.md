---
UID: NS:vmgenerationcounter._VM_GENCOUNTER
title: VM_GENCOUNTER (vmgenerationcounter.h)
description: Describes a virtual machine generation identifier.
helpviewer_keywords: ["*PVM_GENCOUNTER","PVM_GENCOUNTER","PVM_GENCOUNTER structure pointer","VM_GENCOUNTER","VM_GENCOUNTER structure","hyperv.vm_gencounter","vmgenerationcounter/PVM_GENCOUNTER","vmgenerationcounter/VM_GENCOUNTER"]
old-location: hyperv\vm_gencounter.htm
tech.root: hyperv
ms.assetid: F1F2C867-2607-40AD-92B7-E7C07304D885
ms.date: 12/05/2018
ms.keywords: '*PVM_GENCOUNTER, PVM_GENCOUNTER, PVM_GENCOUNTER structure pointer, VM_GENCOUNTER, VM_GENCOUNTER structure, hyperv.vm_gencounter, vmgenerationcounter/PVM_GENCOUNTER, vmgenerationcounter/VM_GENCOUNTER'
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
targetos: Windows
req.typenames: VM_GENCOUNTER, *PVM_GENCOUNTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VM_GENCOUNTER
 - vmgenerationcounter/_VM_GENCOUNTER
 - PVM_GENCOUNTER
 - vmgenerationcounter/PVM_GENCOUNTER
 - VM_GENCOUNTER
 - vmgenerationcounter/VM_GENCOUNTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmgenerationcounter.h
api_name:
 - VM_GENCOUNTER
---

# VM_GENCOUNTER structure


## -description

Describes a virtual machine generation identifier.

## -struct-fields

### -field GenerationCount

The low 64 bits of the virtual machine generation identifier.

### -field GenerationCountHigh

The high 64 bits of the virtual machine generation identifier.

## -remarks

For info about the virtual machine generation identifier, see <a href="/windows/desktop/HyperV_v2/virtual-machine-generation-identifier">Virtual machine generation identifier</a>.

## -see-also

<a href="/windows/desktop/api/vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read">IOCTL_VMGENCOUNTER_READ</a>