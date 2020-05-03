---
UID: NE:comsvcs.tagCRMFLAGS
title: CRMFLAGS (comsvcs.h)
description: Provides information about when a particular log record to the CRM compensator was written.helpviewer_keywords: ["CRMFLAGS","CRMFLAGS enumeration [COM+]","CRMFLAG_FORGETTARGET","CRMFLAG_REPLAYINPROGRESS","CRMFLAG_WRITTENDURINGABORT","CRMFLAG_WRITTENDURINGCOMMIT","CRMFLAG_WRITTENDURINGPREPARE","CRMFLAG_WRITTENDURINGRECOVERY","CRMFLAG_WRITTENDURINGREPLAY","_cos_CRMFLAGS","comsvcs/CRMFLAGS","comsvcs/CRMFLAG_FORGETTARGET","comsvcs/CRMFLAG_REPLAYINPROGRESS","comsvcs/CRMFLAG_WRITTENDURINGABORT","comsvcs/CRMFLAG_WRITTENDURINGCOMMIT","comsvcs/CRMFLAG_WRITTENDURINGPREPARE","comsvcs/CRMFLAG_WRITTENDURINGRECOVERY","comsvcs/CRMFLAG_WRITTENDURINGREPLAY","cos.crmflags"]
old-location: cos\crmflags.htm
tech.root: cossdk
ms.assetid: ef41c99c-9f57-430f-af43-ba0ee1eb7a03
ms.date: 12/05/2018
ms.keywords: CRMFLAGS, CRMFLAGS enumeration [COM+], CRMFLAG_FORGETTARGET, CRMFLAG_REPLAYINPROGRESS, CRMFLAG_WRITTENDURINGABORT, CRMFLAG_WRITTENDURINGCOMMIT, CRMFLAG_WRITTENDURINGPREPARE, CRMFLAG_WRITTENDURINGRECOVERY, CRMFLAG_WRITTENDURINGREPLAY, _cos_CRMFLAGS, comsvcs/CRMFLAGS, comsvcs/CRMFLAG_FORGETTARGET, comsvcs/CRMFLAG_REPLAYINPROGRESS, comsvcs/CRMFLAG_WRITTENDURINGABORT, comsvcs/CRMFLAG_WRITTENDURINGCOMMIT, comsvcs/CRMFLAG_WRITTENDURINGPREPARE, comsvcs/CRMFLAG_WRITTENDURINGRECOVERY, comsvcs/CRMFLAG_WRITTENDURINGREPLAY, cos.crmflags
f1_keywords:
- comsvcs/CRMFLAGS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ComSvcs.h
api_name:
- CRMFLAGS
targetos: Windows
req.typenames: CRMFLAGS
req.redist: 
ms.custom: 19H1
---

# CRMFLAGS enumeration


## -description


Provides information about when a particular log record to the CRM compensator was written.


## -enum-fields




### -field CRMFLAG_FORGETTARGET


### -field CRMFLAG_WRITTENDURINGPREPARE

The record was written during prepare.


### -field CRMFLAG_WRITTENDURINGCOMMIT

The record was written during commit.


### -field CRMFLAG_WRITTENDURINGABORT

The record was written during abort.


### -field CRMFLAG_WRITTENDURINGRECOVERY

The record was written during recovery.


### -field CRMFLAG_WRITTENDURINGREPLAY

The record was written during replay.


### -field CRMFLAG_REPLAYINPROGRESS


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-crmlogrecordread">CrmLogRecordRead</a>
 

 

