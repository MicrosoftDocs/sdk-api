---
UID: NE:vdshwprv._VDS_MAINTENANCE_OPERATION
title: VDS_MAINTENANCE_OPERATION (vdshwprv.h)
description: Defines the set of valid subsystem maintenance operations.
helpviewer_keywords: ["BeepAlarm","BlinkLight","Ping","SpinDown","SpinUp","VDS_MAINTENANCE_OPERATION","VDS_MAINTENANCE_OPERATION enumeration [VDS]","base.vds_maintenance_operation","vds/BeepAlarm","vds/BlinkLight","vds/Ping","vds/SpinDown","vds/SpinUp","vds/VDS_MAINTENANCE_OPERATION","vdshwprv/BeepAlarm","vdshwprv/BlinkLight","vdshwprv/Ping","vdshwprv/SpinDown","vdshwprv/SpinUp","vdshwprv/VDS_MAINTENANCE_OPERATION"]
old-location: base\vds_maintenance_operation.htm
tech.root: base
ms.assetid: 29bc5eb3-2e4b-4ca1-8b0a-9b43d2723e56
ms.date: 12/05/2018
ms.keywords: BeepAlarm, BlinkLight, Ping, SpinDown, SpinUp, VDS_MAINTENANCE_OPERATION, VDS_MAINTENANCE_OPERATION enumeration [VDS], base.vds_maintenance_operation, vds/BeepAlarm, vds/BlinkLight, vds/Ping, vds/SpinDown, vds/SpinUp, vds/VDS_MAINTENANCE_OPERATION, vdshwprv/BeepAlarm, vdshwprv/BlinkLight, vdshwprv/Ping, vdshwprv/SpinDown, vdshwprv/SpinUp, vdshwprv/VDS_MAINTENANCE_OPERATION
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
targetos: Windows
req.typenames: VDS_MAINTENANCE_OPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_MAINTENANCE_OPERATION
 - vdshwprv/_VDS_MAINTENANCE_OPERATION
 - VDS_MAINTENANCE_OPERATION
 - vdshwprv/VDS_MAINTENANCE_OPERATION
dev_langs:
 - c++
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
---

# VDS_MAINTENANCE_OPERATION enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid subsystem maintenance operations.

## -enum-fields

### -field BlinkLight:1

Blinks a light on a drive.

### -field BeepAlarm:2

Beeps an alarm on a drive.

### -field SpinDown:3

Slows the spinning of a drive such that the drive enters an idle state. Typically used for the purpose of saving power.

### -field SpinUp:4

Starts the spinning of a drive in preparation for data reads.

### -field Ping:5

Pings a drive.

## -remarks

The  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-startmaintenance">IVdsMaintenance::StartMaintenance</a>, <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-stopmaintenance">IVdsMaintenance::StopMaintenance</a>, and <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-pulsemaintenance">IVdsMaintenance::PulseMaintenance</a> methods pass a <b>VDS_MAINTENANCE_OPERATION</b> value as an argument to specify operation details.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_MAINTENANCE_OPERATION</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_MAINTENANCE_OPERATION</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-pulsemaintenance">IVdsMaintenance::PulseMaintenance</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-startmaintenance">IVdsMaintenance::StartMaintenance</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-stopmaintenance">IVdsMaintenance::StopMaintenance</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
