---
UID: NE:comsvcs.tagCRMFLAGS
title: CRMFLAGS (comsvcs.h)
description: Provides information about when a particular log record to the CRM compensator was written.
helpviewer_keywords: ["CRMFLAGS","CRMFLAGS enumeration [COM+]","CRMFLAG_FORGETTARGET","CRMFLAG_REPLAYINPROGRESS","CRMFLAG_WRITTENDURINGABORT","CRMFLAG_WRITTENDURINGCOMMIT","CRMFLAG_WRITTENDURINGPREPARE","CRMFLAG_WRITTENDURINGRECOVERY","CRMFLAG_WRITTENDURINGREPLAY","_cos_CRMFLAGS","comsvcs/CRMFLAGS","comsvcs/CRMFLAG_FORGETTARGET","comsvcs/CRMFLAG_REPLAYINPROGRESS","comsvcs/CRMFLAG_WRITTENDURINGABORT","comsvcs/CRMFLAG_WRITTENDURINGCOMMIT","comsvcs/CRMFLAG_WRITTENDURINGPREPARE","comsvcs/CRMFLAG_WRITTENDURINGRECOVERY","comsvcs/CRMFLAG_WRITTENDURINGREPLAY","cos.crmflags"]
old-location: cos\crmflags.htm
tech.root: cos
ms.assetid: ef41c99c-9f57-430f-af43-ba0ee1eb7a03
ms.date: 12/05/2018
ms.keywords: CRMFLAGS, CRMFLAGS enumeration [COM+], CRMFLAG_FORGETTARGET, CRMFLAG_REPLAYINPROGRESS, CRMFLAG_WRITTENDURINGABORT, CRMFLAG_WRITTENDURINGCOMMIT, CRMFLAG_WRITTENDURINGPREPARE, CRMFLAG_WRITTENDURINGRECOVERY, CRMFLAG_WRITTENDURINGREPLAY, _cos_CRMFLAGS, comsvcs/CRMFLAGS, comsvcs/CRMFLAG_FORGETTARGET, comsvcs/CRMFLAG_REPLAYINPROGRESS, comsvcs/CRMFLAG_WRITTENDURINGABORT, comsvcs/CRMFLAG_WRITTENDURINGCOMMIT, comsvcs/CRMFLAG_WRITTENDURINGPREPARE, comsvcs/CRMFLAG_WRITTENDURINGRECOVERY, comsvcs/CRMFLAG_WRITTENDURINGREPLAY, cos.crmflags
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: CRMFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCRMFLAGS
 - comsvcs/tagCRMFLAGS
 - CRMFLAGS
 - comsvcs/CRMFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CRMFLAGS
---

# CRMFLAGS enumeration


## -description

Provides information about when a particular log record to the CRM compensator was written.

## -enum-fields

### -field CRMFLAG_FORGETTARGET:0x1

### -field CRMFLAG_WRITTENDURINGPREPARE:0x2

The record was written during prepare.

### -field CRMFLAG_WRITTENDURINGCOMMIT:0x4

The record was written during commit.

### -field CRMFLAG_WRITTENDURINGABORT:0x8

The record was written during abort.

### -field CRMFLAG_WRITTENDURINGRECOVERY:0x10

The record was written during recovery.

### -field CRMFLAG_WRITTENDURINGREPLAY:0x20

The record was written during replay.

### -field CRMFLAG_REPLAYINPROGRESS:0x40

## -see-also

<a href="/windows/desktop/api/comsvcs/ns-comsvcs-crmlogrecordread">CrmLogRecordRead</a>
