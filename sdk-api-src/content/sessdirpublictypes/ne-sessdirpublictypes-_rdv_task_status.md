---
UID: NE:sessdirpublictypes._RDV_TASK_STATUS
title: "_RDV_TASK_STATUS"
author: windows-driver-content
description: Used with the IRDVTaskPluginNotifySink::OnTaskStateChange method to indicate the status of a task.
old-location: termserv\rdv_task_status.htm
old-project: TermServ
ms.assetid: 69278A29-9100-4855-B5B3-C790563B8B72
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: RDV_TASK_STATUS, RDV_TASK_STATUS enumeration [Remote Desktop Services], RDV_TASK_STATUS_APPLYING, RDV_TASK_STATUS_DOWNLOADING, RDV_TASK_STATUS_FAILED, RDV_TASK_STATUS_REBOOTED, RDV_TASK_STATUS_REBOOTING, RDV_TASK_STATUS_SEARCHING, RDV_TASK_STATUS_SUCCESS, RDV_TASK_STATUS_TIMEOUT, RDV_TASK_STATUS_UNKNOWN, _RDV_TASK_STATUS, sessdirpublictypes/RDV_TASK_STATUS, sessdirpublictypes/RDV_TASK_STATUS_APPLYING, sessdirpublictypes/RDV_TASK_STATUS_DOWNLOADING, sessdirpublictypes/RDV_TASK_STATUS_FAILED, sessdirpublictypes/RDV_TASK_STATUS_REBOOTED, sessdirpublictypes/RDV_TASK_STATUS_REBOOTING, sessdirpublictypes/RDV_TASK_STATUS_SEARCHING, sessdirpublictypes/RDV_TASK_STATUS_SUCCESS, sessdirpublictypes/RDV_TASK_STATUS_TIMEOUT, sessdirpublictypes/RDV_TASK_STATUS_UNKNOWN, termserv.rdv_task_status
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: sessdirpublictypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SessDirPublicTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RDV_TASK_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	SessDirPublicTypes.h
api_name:
-	RDV_TASK_STATUS
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RDV_TASK_STATUS enumeration


## -description


Used with the <a href="https://msdn.microsoft.com/3021ea7a-2627-48d1-8df5-c40e7a9b51c5">IRDVTaskPluginNotifySink::OnTaskStateChange</a> method to indicate the status of a task.


## -enum-fields




### -field RDV_TASK_STATUS_UNKNOWN

The task state cannot be determined.


### -field RDV_TASK_STATUS_SEARCHING

Searching for applicable tasks.


### -field RDV_TASK_STATUS_DOWNLOADING

Downloading tasks.


### -field RDV_TASK_STATUS_APPLYING

Performing tasks.


### -field RDV_TASK_STATUS_REBOOTING

Rebooting. The task may or may not be complete.


### -field RDV_TASK_STATUS_REBOOTED

Reboot completed. The task may or may not be complete.


### -field RDV_TASK_STATUS_SUCCESS

Task completed successfully.


### -field RDV_TASK_STATUS_FAILED

Task failed.


### -field RDV_TASK_STATUS_TIMEOUT

Task did not finish in the allotted time.


## -see-also




<a href="https://msdn.microsoft.com/3021ea7a-2627-48d1-8df5-c40e7a9b51c5">IRDVTaskPluginNotifySink::OnTaskStateChange</a>
 

 

