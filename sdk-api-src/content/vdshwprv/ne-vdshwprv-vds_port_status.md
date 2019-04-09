---
UID: NE:vdshwprv._VDS_PORT_STATUS
title: VDS_PORT_STATUS (vdshwprv.h)
author: windows-sdk-content
description: Defines the set of object status values for a port.
old-location: base\vds_port_status.htm
tech.root: VDS
ms.assetid: 6e363020-caf4-4028-abd5-7f311edb2e69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVDS_PORT_STATUS, VDS_PORT_STATUS, VDS_PORT_STATUS enumeration [VDS], VDS_PRS_FAILED, VDS_PRS_NOT_READY, VDS_PRS_OFFLINE, VDS_PRS_ONLINE, VDS_PRS_REMOVED, VDS_PRS_UNKNOWN, base.vds_port_status, vds/VDS_PORT_STATUS, vds/VDS_PRS_FAILED, vds/VDS_PRS_NOT_READY, vds/VDS_PRS_OFFLINE, vds/VDS_PRS_ONLINE, vds/VDS_PRS_REMOVED, vds/VDS_PRS_UNKNOWN, vdshwprv/VDS_PORT_STATUS, vdshwprv/VDS_PRS_FAILED, vdshwprv/VDS_PRS_NOT_READY, vdshwprv/VDS_PRS_OFFLINE, vdshwprv/VDS_PRS_ONLINE, vdshwprv/VDS_PRS_REMOVED, vdshwprv/VDS_PRS_UNKNOWN"
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
 - VDS_PORT_STATUS
product: Windows
targetos: Windows
req.typenames: VDS_PORT_STATUS, *PVDS_PORT_STATUS
req.redist: 
---

# VDS_PORT_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a port.


## -enum-fields




### -field VDS_PRS_UNKNOWN

The status of the port cannot be determined.


### -field VDS_PRS_ONLINE

The port is physically present and in use. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value associated with this port status can be any value except <b>VDS_H_FAILED</b>.


### -field VDS_PRS_NOT_READY

The port is busy. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value can be any value except <b>VDS_H_FAILED</b>.


### -field VDS_PRS_OFFLINE

Either the port or its controller is physically present but not available for use. For example, the port or its controller has been set to the inactive state. When this status is set,  a <b>VDS_NF_PORT_REMOVED</b> notification is sent. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value can be any value.


### -field VDS_PRS_FAILED

The port has failed. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value should be <b>VDS_H_FAILED</b> or <b>VDS_H_FAILING</b>.


### -field VDS_PRS_REMOVED

The port's controller has been physically removed from the subsystem.  When this status is set, a <b>VDS_NF_PORT_DEPART</b> notification is sent.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



The  <a href="https://msdn.microsoft.com/40f81f31-3776-4685-8b79-c047c669b2bb">VDS_PORT_PROP</a> structure includes a <b>VDS_PORT_STATUS</b> value as a member to indicate the current status of a port.

If your application encounters a <b>VDS_PORT_STATUS</b> value that it does not recognize, it should display the port status as unknown. It should not attempt to map the unrecognized port status to another port status.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PORT_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PORT_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/40f81f31-3776-4685-8b79-c047c669b2bb">VDS_PORT_PROP</a>
 

 

