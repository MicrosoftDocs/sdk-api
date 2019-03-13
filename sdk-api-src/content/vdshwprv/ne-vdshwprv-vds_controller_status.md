---
UID: NE:vdshwprv._VDS_CONTROLLER_STATUS
title: VDS_CONTROLLER_STATUS
author: windows-sdk-content
description: Defines the set of object status values for a controller.
old-location: base\vds_controller_status.htm
tech.root: VDS
ms.assetid: a888fcb7-83f5-40c1-9f24-efa929aa9f6a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVDS_CONTROLLER_STATUS, VDS_CONTROLLER_STATUS, VDS_CONTROLLER_STATUS enumeration [VDS], VDS_CS_FAILED, VDS_CS_NOT_READY, VDS_CS_OFFLINE, VDS_CS_ONLINE, VDS_CS_REMOVED, VDS_CS_UNKNOWN, base.vds_controller_status, vds/VDS_CONTROLLER_STATUS, vds/VDS_CS_FAILED, vds/VDS_CS_NOT_READY, vds/VDS_CS_OFFLINE, vds/VDS_CS_ONLINE, vds/VDS_CS_REMOVED, vds/VDS_CS_UNKNOWN, vdshwprv/VDS_CONTROLLER_STATUS, vdshwprv/VDS_CS_FAILED, vdshwprv/VDS_CS_NOT_READY, vdshwprv/VDS_CS_OFFLINE, vdshwprv/VDS_CS_ONLINE, vdshwprv/VDS_CS_REMOVED, vdshwprv/VDS_CS_UNKNOWN"
ms.topic: enum
req.header: vdshwprv.h
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
 - VDS_CONTROLLER_STATUS
product: Windows
targetos: Windows
req.typenames: VDS_CONTROLLER_STATUS, *PVDS_CONTROLLER_STATUS
req.redist: 
---

# VDS_CONTROLLER_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a controller.


## -enum-fields




### -field VDS_CS_UNKNOWN

The status of the controller cannot be determined.


### -field VDS_CS_ONLINE

The controller is physically present and in use. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value associated with this controller status can be any value except <b>VDS_H_FAILED</b>.


### -field VDS_CS_NOT_READY

The controller is busy. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value can be any value except <b>VDS_H_FAILED</b>.


### -field VDS_CS_OFFLINE

The controller is physically present but not available for use. For example, the controller has been set to the inactive state. When this controller status is set, a <b>VDS_NF_CONTROLLER_REMOVED</b> notification is sent.  The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value can be any value.


### -field VDS_CS_FAILED

The controller has failed. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value should be <b>VDS_H_FAILED</b> or <b>VDS_H_FAILING</b>.


### -field VDS_CS_REMOVED

The controller has been physically unplugged from the subsystem. When this status is set, a <b>VDS_NF_CONTROLLER_DEPART</b> notification is sent.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



The <a href="https://msdn.microsoft.com/f9bae451-ef47-46ad-a11e-b7b36a031a8a">IVdsController::SetStatus</a>method passes a <b>VDS_CONTROLLER_STATUS</b> value as an argument to set the status of a controller, and  the <a href="https://msdn.microsoft.com/b9da3920-9bae-4198-ba0d-a0755aee15e4">VDS_CONTROLLER_PROP</a> structure includes a <b>VDS_CONTROLLER_STATUS</b> value as a member to indicate the current status.

If your application encounters a <b>VDS_CONTROLLER_STATUS</b> value that it does not recognize, it should display the controller status as unknown. It should not attempt to map the unrecognized controller status to another controller status.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_CONTROLLER_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_CONTROLLER_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f9bae451-ef47-46ad-a11e-b7b36a031a8a">IVdsController::SetStatus</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/b9da3920-9bae-4198-ba0d-a0755aee15e4">VDS_CONTROLLER_PROP</a>
 

 

