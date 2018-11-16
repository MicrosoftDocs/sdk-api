---
UID: NE:comsvcs.tagCRMFLAGS
title: tagCRMFLAGS
author: windows-sdk-content
description: Provides information about when a particular log record to the CRM compensator was written.
old-location: cos\crmflags.htm
tech.root: cossdk
ms.assetid: ef41c99c-9f57-430f-af43-ba0ee1eb7a03
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CRMFLAGS, CRMFLAGS enumeration [COM+], CRMFLAG_FORGETTARGET, CRMFLAG_REPLAYINPROGRESS, CRMFLAG_WRITTENDURINGABORT, CRMFLAG_WRITTENDURINGCOMMIT, CRMFLAG_WRITTENDURINGPREPARE, CRMFLAG_WRITTENDURINGRECOVERY, CRMFLAG_WRITTENDURINGREPLAY, _cos_CRMFLAGS, comsvcs/CRMFLAGS, comsvcs/CRMFLAG_FORGETTARGET, comsvcs/CRMFLAG_REPLAYINPROGRESS, comsvcs/CRMFLAG_WRITTENDURINGABORT, comsvcs/CRMFLAG_WRITTENDURINGCOMMIT, comsvcs/CRMFLAG_WRITTENDURINGPREPARE, comsvcs/CRMFLAG_WRITTENDURINGRECOVERY, comsvcs/CRMFLAG_WRITTENDURINGREPLAY, cos.crmflags, tagCRMFLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: CRMFLAGS
req.redist: 
---

# tagCRMFLAGS enumeration


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




<a href="https://msdn.microsoft.com/0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6">CrmLogRecordRead</a>
 

 

