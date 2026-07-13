---
UID: NS:iscsidsc.ISCSI_TARGET_MAPPINGW
title: ISCSI_TARGET_MAPPINGW (iscsidsc.h)
description: ISCSI_TARGET_MAPPING. (Unicode)
helpviewer_keywords: ["*PISCSI_TARGET_MAPPINGW","ISCSI_TARGET_MAPPING","ISCSI_TARGET_MAPPING structure [iSCSI Discovery Library API]","ISCSI_TARGET_MAPPINGA","ISCSI_TARGET_MAPPINGW","PISCSI_TARGET_MAPPING","PISCSI_TARGET_MAPPING structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_target_mapping","iscsidsc/ISCSI_TARGET_MAPPING","iscsidsc/ISCSI_TARGET_MAPPINGA","iscsidsc/ISCSI_TARGET_MAPPINGW","iscsidsc/PISCSI_TARGET_MAPPING"]
old-location: iscsidisc\iscsi_target_mapping.htm
tech.root: iSCSIDisc
ms.assetid: bdc27e67-1d64-42cd-adfa-a792012b7142
ms.date: 12/05/2018
ms.keywords: '*PISCSI_TARGET_MAPPINGW, ISCSI_TARGET_MAPPING, ISCSI_TARGET_MAPPING structure [iSCSI Discovery Library API], ISCSI_TARGET_MAPPINGA, ISCSI_TARGET_MAPPINGW, PISCSI_TARGET_MAPPING, PISCSI_TARGET_MAPPING structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_target_mapping, iscsidsc/ISCSI_TARGET_MAPPING, iscsidsc/ISCSI_TARGET_MAPPINGA, iscsidsc/ISCSI_TARGET_MAPPINGW, iscsidsc/PISCSI_TARGET_MAPPING'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_TARGET_MAPPINGW (Unicode) and ISCSI_TARGET_MAPPINGA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ISCSI_TARGET_MAPPINGW, *PISCSI_TARGET_MAPPINGW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_TARGET_MAPPINGW
 - iscsidsc/PISCSI_TARGET_MAPPINGW
 - ISCSI_TARGET_MAPPINGW
 - iscsidsc/ISCSI_TARGET_MAPPINGW
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
 - ISCSI_TARGET_MAPPING
 - ISCSI_TARGET_MAPPINGA
 - ISCSI_TARGET_MAPPINGW
---

# ISCSI_TARGET_MAPPINGW structure


## -description

The 		ISCSI_TARGET_MAPPING structure contains information about a target and the Host-Bus  Adapters (HBAs) and buses through which the target is reached.

## -struct-fields

### -field InitiatorName

A string representing the name of the HBA initiator through which the target is accessed.

### -field TargetName

A string representing the target name.

### -field OSDeviceName

A string representing the device name of the HBA initiator; for example '<b>\device\ScsiPort3</b>'.

### -field SessionId

A <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> structure containing information that uniquely identifies the session..

### -field OSBusNumber

The bus number used by the initiator as the local SCSI address of the target.

### -field OSTargetNumber

The target number used by the initiator as the local SCSI address of the target.

### -field LUNCount

The number of logical units (LUN) on the target.

### -field LUNList

A list of SCSI_LUN_LIST structures that contain information about the LUNs associated with the target.

### -field size_is

### -field size_is.LUNCount

## -see-also

<a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ISCSI_TARGET_MAPPING as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

