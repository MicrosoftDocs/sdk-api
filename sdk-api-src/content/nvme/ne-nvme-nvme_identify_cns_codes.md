---
UID: NE:nvme.NVME_IDENTIFY_CNS_CODES
tech.root: fs
title: NVME_IDENTIFY_CNS_CODES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the type of controller or namespace information that will be returned in the Controller or Namespace Structure (CNS) member of the NVME_CDW10_IDENTIFY structure.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_IDENTIFY_CNS_CODES
f1_keywords:
 - NVME_IDENTIFY_CNS_CODES
 - nvme/NVME_IDENTIFY_CNS_CODES
dev_langs:
 - c++
---

# NVME_IDENTIFY_CNS_CODES enumeration


## -description

Contains values that indicate the type of controller or namespace information that will be returned in the Controller or Namespace Structure (**CNS**) member of the Identify command [NVME_CDW10_IDENTIFY](ns-nvme-nvme_command_dword0.md) structure.

## -enum-fields

### -field NVME_IDENTIFY_CNS_SPECIFIC_NAMESPACE

Information for a specific namespace will be returned.

The Identify Namespace [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md) structure is returned to the host for the namespace specified in the Namespace Identifier (**NSID**) member of the [NVME_COMMAND](ns-nvme-nvme_command.md) structure, if the namespace is attached to this controller.

If the specified namespace is an inactive namespace ID, then the controller returns a zero filled data structure.

If the controller supports Namespace Management and **NSID** is set to `FFFFFFFFh`, the controller returns an **NVME_IDENTIFY_NAMESPACE_DATA** that specifies capabilities that are common across namespaces.

### -field NVME_IDENTIFY_CNS_CONTROLLER

Information for a controller will be returned to the host in an Identify Controller [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) data structure.

### -field NVME_IDENTIFY_CNS_ACTIVE_NAMESPACES

A list of active namespaces will be returned.

A list of up to 1024 active namespace IDs is returned to the host containing active namespaces with a namespace identifier greater than the value specified in the **NSID** member of the **NVME_COMMAND** structure.

### -field NVME_IDENTIFY_CNS_DESCRIPTOR_NAMESPACE

Information for a descriptor namespace will be returned.

### -field NVME_IDENTIFY_CNS_NVM_SET

An [NVM_SET_LIST](ns-nvme-nvm_set_list.md) will be returned.

## -remarks

## -see-also

[NVME_COMMAND](ns-nvme-nvme_command.md)
[NVME_CDW10_IDENTIFY](ns-nvme-nvme_command_dword0.md)
[NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md)
[NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)
[NVM_SET_LIST](ns-nvme-nvm_set_list.md)

