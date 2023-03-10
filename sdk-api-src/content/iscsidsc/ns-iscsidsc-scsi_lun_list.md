---
UID: NS:iscsidsc.SCSI_LUN_LIST
title: SCSI_LUN_LIST (iscsidsc.h)
description: SCSI_LUN_LIST structure is used to construct a list of logical unit numbers (LUNs) associated with target devices.
helpviewer_keywords: ["*PSCSI_LUN_LIST","PSCSI_LUN_LIST","PSCSI_LUN_LIST structure pointer [iSCSI Discovery Library API]","SCSI_LUN_LIST","SCSI_LUN_LIST structure [iSCSI Discovery Library API]","iscsidisc.scsi_lun_list","iscsidsc/PSCSI_LUN_LIST","iscsidsc/SCSI_LUN_LIST"]
old-location: iscsidisc\scsi_lun_list.htm
tech.root: iSCSIDisc
ms.assetid: b0ff4b28-887c-42bf-bb7b-da23c231ff4e
ms.date: 12/05/2018
ms.keywords: '*PSCSI_LUN_LIST, PSCSI_LUN_LIST, PSCSI_LUN_LIST structure pointer [iSCSI Discovery Library API], SCSI_LUN_LIST, SCSI_LUN_LIST structure [iSCSI Discovery Library API], iscsidisc.scsi_lun_list, iscsidsc/PSCSI_LUN_LIST, iscsidsc/SCSI_LUN_LIST'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SCSI_LUN_LIST, *PSCSI_LUN_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSCSI_LUN_LIST
 - iscsidsc/PSCSI_LUN_LIST
 - SCSI_LUN_LIST
 - iscsidsc/SCSI_LUN_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - SCSI_LUN_LIST
---

# SCSI_LUN_LIST structure


## -description

The <b>SCSI_LUN_LIST</b> structure is used to construct a list of logical unit numbers (LUNs) associated with target devices.

## -struct-fields

### -field OSLUN

The LUN assigned by the operating system to the target device when it was enumerated by the initiator Host Bus Adapter (HBA).

### -field TargetLUN

The LUN assigned by the target subsystem to the target device.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a>

