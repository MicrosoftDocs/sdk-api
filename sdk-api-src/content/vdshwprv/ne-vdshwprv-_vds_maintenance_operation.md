---
UID: NE:vdshwprv._VDS_MAINTENANCE_OPERATION
title: "_VDS_MAINTENANCE_OPERATION"
author: windows-sdk-content
description: Defines the set of valid subsystem maintenance operations.
old-location: base\vds_maintenance_operation.htm
tech.root: VDS
ms.assetid: 29bc5eb3-2e4b-4ca1-8b0a-9b43d2723e56
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BeepAlarm, BlinkLight, Ping, SpinDown, SpinUp, VDS_MAINTENANCE_OPERATION, VDS_MAINTENANCE_OPERATION enumeration [VDS], _VDS_MAINTENANCE_OPERATION, base.vds_maintenance_operation, vds/BeepAlarm, vds/BlinkLight, vds/Ping, vds/SpinDown, vds/SpinUp, vds/VDS_MAINTENANCE_OPERATION, vdshwprv/BeepAlarm, vdshwprv/BlinkLight, vdshwprv/Ping, vdshwprv/SpinDown, vdshwprv/SpinUp, vdshwprv/VDS_MAINTENANCE_OPERATION
ms.prod: windows
ms.technology: windows-sdk
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
 - VDS_MAINTENANCE_OPERATION
product: Windows
targetos: Windows
req.typenames: VDS_MAINTENANCE_OPERATION
req.redist: 
---

# _VDS_MAINTENANCE_OPERATION enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid subsystem maintenance operations.


## -enum-fields




### -field BlinkLight

Blinks a light on a drive.


### -field BeepAlarm

Beeps an alarm on a drive.


### -field SpinDown

Slows the spinning of a drive such that the drive enters an idle state. Typically used for the purpose of saving power.


### -field SpinUp

Starts the spinning of a drive in preparation for data reads.


### -field Ping

Pings a drive.


## -remarks



The  <a href="https://msdn.microsoft.com/8d2e1022-ae79-4f71-a488-2c86b43b2a7f">IVdsMaintenance::StartMaintenance</a>, <a href="https://msdn.microsoft.com/542f84d7-eb97-4738-b7c0-1c95bc5e063c">IVdsMaintenance::StopMaintenance</a>, and <a href="https://msdn.microsoft.com/057424eb-c491-4295-b2a7-cf983902c667">IVdsMaintenance::PulseMaintenance</a> methods pass a <b>VDS_MAINTENANCE_OPERATION</b> value as an argument to specify operation details.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_MAINTENANCE_OPERATION</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_MAINTENANCE_OPERATION</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/057424eb-c491-4295-b2a7-cf983902c667">IVdsMaintenance::PulseMaintenance</a>



<a href="https://msdn.microsoft.com/8d2e1022-ae79-4f71-a488-2c86b43b2a7f">IVdsMaintenance::StartMaintenance</a>



<a href="https://msdn.microsoft.com/542f84d7-eb97-4738-b7c0-1c95bc5e063c">IVdsMaintenance::StopMaintenance</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

