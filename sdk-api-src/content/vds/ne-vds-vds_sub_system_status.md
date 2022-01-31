---
UID: NE:vds._VDS_SUB_SYSTEM_STATUS
title: VDS_SUB_SYSTEM_STATUS (vds.h)
description: Defines the set of object status values for a subsystem.
helpviewer_keywords: ["*PVDS_SUB_SYSTEM_STATUS","VDS_SSS_FAILED","VDS_SSS_NOT_READY","VDS_SSS_OFFLINE","VDS_SSS_ONLINE","VDS_SSS_PARTIALLY_MANAGED","VDS_SSS_UNKNOWN","VDS_SUB_SYSTEM_STATUS","VDS_SUB_SYSTEM_STATUS enumeration [VDS]","base.vds_sub_system_status","vds/VDS_SSS_FAILED","vds/VDS_SSS_NOT_READY","vds/VDS_SSS_OFFLINE","vds/VDS_SSS_ONLINE","vds/VDS_SSS_PARTIALLY_MANAGED","vds/VDS_SSS_UNKNOWN","vds/VDS_SUB_SYSTEM_STATUS","vdshwprv/VDS_SSS_FAILED","vdshwprv/VDS_SSS_NOT_READY","vdshwprv/VDS_SSS_OFFLINE","vdshwprv/VDS_SSS_ONLINE","vdshwprv/VDS_SSS_PARTIALLY_MANAGED","vdshwprv/VDS_SSS_UNKNOWN","vdshwprv/VDS_SUB_SYSTEM_STATUS"]
old-location: base\vds_sub_system_status.htm
tech.root: base
ms.assetid: 3393ff1f-df0f-4053-9127-d99196660f4b
ms.date: 12/05/2018
ms.keywords: '*PVDS_SUB_SYSTEM_STATUS, VDS_SSS_FAILED, VDS_SSS_NOT_READY, VDS_SSS_OFFLINE, VDS_SSS_ONLINE, VDS_SSS_PARTIALLY_MANAGED, VDS_SSS_UNKNOWN, VDS_SUB_SYSTEM_STATUS, VDS_SUB_SYSTEM_STATUS enumeration [VDS], base.vds_sub_system_status, vds/VDS_SSS_FAILED, vds/VDS_SSS_NOT_READY, vds/VDS_SSS_OFFLINE, vds/VDS_SSS_ONLINE, vds/VDS_SSS_PARTIALLY_MANAGED, vds/VDS_SSS_UNKNOWN, vds/VDS_SUB_SYSTEM_STATUS, vdshwprv/VDS_SSS_FAILED, vdshwprv/VDS_SSS_NOT_READY, vdshwprv/VDS_SSS_OFFLINE, vdshwprv/VDS_SSS_ONLINE, vdshwprv/VDS_SSS_PARTIALLY_MANAGED, vdshwprv/VDS_SSS_UNKNOWN, vdshwprv/VDS_SUB_SYSTEM_STATUS'
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
targetos: Windows
req.typenames: VDS_SUB_SYSTEM_STATUS, *PVDS_SUB_SYSTEM_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_SUB_SYSTEM_STATUS
 - vds/_VDS_SUB_SYSTEM_STATUS
 - PVDS_SUB_SYSTEM_STATUS
 - vds/PVDS_SUB_SYSTEM_STATUS
 - VDS_SUB_SYSTEM_STATUS
 - vds/VDS_SUB_SYSTEM_STATUS
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
 - VDS_SUB_SYSTEM_STATUS
---

# VDS_SUB_SYSTEM_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   set of object status values for a subsystem.

## -enum-fields

### -field VDS_SSS_UNKNOWN:0

This value is reserved.

### -field VDS_SSS_ONLINE:1

The subsystem is working properly.

### -field VDS_SSS_NOT_READY:2

The subsystem is initializing and not yet ready to work.

### -field VDS_SSS_OFFLINE:4

The subsystem is unavailable. This value indicates either that the subsystem is disconnected or that it has 
      failed so severely that it appears to be disconnected.

### -field VDS_SSS_FAILED:5

The subsystem has failed. This value indicates that the subsystem is not merely 
      disconnected but rather that it has failed.

### -field VDS_SSS_PARTIALLY_MANAGED:9

The subsystem is operating in a degraded state. This means that one or more of the subsystem's subcomponents, such as  disk drives or controllers, are in a failed state.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-setstatus">IVdsSubSystem::SetStatus</a> method passes a <b>VDS_SUB_SYSTEM_STATUS</b> 
    value as an argument to set the status of a subsystem, and the 
    <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure includes a <b>VDS_SUB_SYSTEM_STATUS</b> value 
    as a member to indicate the current status.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_SUB_SYSTEM_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_SUB_SYSTEM_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-setstatus">IVdsSubSystem::SetStatus</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a>
