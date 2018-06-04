---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

