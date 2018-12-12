---
UID: NS:vds._VDS_CONTROLLER_PROP
title: VDS_CONTROLLER_PROP
author: windows-sdk-content
description: Defines the properties of a controller object.
old-location: base\vds_controller_prop.htm
tech.root: vds
ms.assetid: b9da3920-9bae-4198-ba0d-a0755aee15e4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVDS_CONTROLLER_PROP, VDS_CONTROLLER_PROP, VDS_CONTROLLER_PROP structure [VDS], VDS_H_DEGRADED, VDS_H_FAILED, VDS_H_HEALTHY, VDS_H_REPLACED, VDS_H_UNKNOWN, base.vds_controller_prop, vds/_VDS_CONTROLLER_PROP, vdshwprv/_VDS_CONTROLLER_PROP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_CONTROLLER_PROP
product: Windows
targetos: Windows
req.typenames: VDS_CONTROLLER_PROP, *PVDS_CONTROLLER_PROP
req.redist: 
---

# VDS_CONTROLLER_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="https://msdn.microsoft.com/ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8">controller object</a>.


## -struct-fields




### -field id

The GUID of the controller object.


### -field pwszFriendlyName

The name of the controller; a zero-terminated, human-readable string.


### -field pwszIdentification

The subsystem identifier, typically a serial number; a zero-terminated, human-readable string.


### -field status

A 
      <a href="https://msdn.microsoft.com/a888fcb7-83f5-40c1-9f24-efa929aa9f6a">VDS_CONTROLLER_STATUS</a> enumeration value that specifies the status of the controller.


### -field health

A 
      <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> enumeration value that specifies the health state of the controller. The following are the valid values for this member.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b><b>VDS_H_REPLACED</b> and <b>VDS_H_DEGRADED</b> are not supported.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILED (8)



#### VDS_H_REPLACED (9)



#### VDS_H_DEGRADED (11)


### -field sNumberOfPorts

The number of ports that the controller contains. Ports are numbered from zero. Hardware providers should set this member to zero for PCI RAID cards.


## -remarks



The <a href="https://msdn.microsoft.com/37230ac4-45f5-46ba-9a1c-072409e9362c">IVdsController::GetProperties</a> 
    method returns this structure to report the properties of a <a href="https://msdn.microsoft.com/ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8">controller object</a>.




## -see-also




<a href="https://msdn.microsoft.com/37230ac4-45f5-46ba-9a1c-072409e9362c">IVdsController::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/a888fcb7-83f5-40c1-9f24-efa929aa9f6a">VDS_CONTROLLER_STATUS</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>
 

 

