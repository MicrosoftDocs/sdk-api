---
UID: NE:vds._VDS_LUN_RESERVE_MODE
title: VDS_LUN_RESERVE_MODE (vds.h)
description: Not supported.This enumeration is reserved for future use.
helpviewer_keywords: ["VDS_LRM_EXCLUSIVE_RO","VDS_LRM_EXCLUSIVE_RW","VDS_LRM_NONE","VDS_LRM_SHARED_RO","VDS_LRM_SHARED_RW","VDS_LUN_RESERVE_MODE","VDS_LUN_RESERVE_MODE enumeration [VDS]","base.vds_lun_reserve_mode","vds/VDS_LRM_EXCLUSIVE_RO","vds/VDS_LRM_EXCLUSIVE_RW","vds/VDS_LRM_NONE","vds/VDS_LRM_SHARED_RO","vds/VDS_LRM_SHARED_RW","vds/VDS_LUN_RESERVE_MODE"]
old-location: base\vds_lun_reserve_mode.htm
tech.root: base
ms.assetid: 198706a4-3692-4f75-bf68-c56671b752a5
ms.date: 12/05/2018
ms.keywords: VDS_LRM_EXCLUSIVE_RO, VDS_LRM_EXCLUSIVE_RW, VDS_LRM_NONE, VDS_LRM_SHARED_RO, VDS_LRM_SHARED_RW, VDS_LUN_RESERVE_MODE, VDS_LUN_RESERVE_MODE enumeration [VDS], base.vds_lun_reserve_mode, vds/VDS_LRM_EXCLUSIVE_RO, vds/VDS_LRM_EXCLUSIVE_RW, vds/VDS_LRM_NONE, vds/VDS_LRM_SHARED_RO, vds/VDS_LRM_SHARED_RW, vds/VDS_LUN_RESERVE_MODE
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
req.typenames: VDS_LUN_RESERVE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_RESERVE_MODE
 - vds/_VDS_LUN_RESERVE_MODE
 - VDS_LUN_RESERVE_MODE
 - vds/VDS_LUN_RESERVE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_LUN_RESERVE_MODE
---

# VDS_LUN_RESERVE_MODE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Not supported.

This enumeration is reserved for future use.

## -enum-fields

### -field VDS_LRM_NONE:0

This value is reserved.

### -field VDS_LRM_EXCLUSIVE_RW:1

This value is reserved.

### -field VDS_LRM_EXCLUSIVE_RO:2

This value is reserved.

### -field VDS_LRM_SHARED_RO:3

This value is reserved.

### -field VDS_LRM_SHARED_RW:4

This value is reserved.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_RESERVE_MODE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_RESERVE_MODE</b> enumeration constant.</div>
<div> </div>
