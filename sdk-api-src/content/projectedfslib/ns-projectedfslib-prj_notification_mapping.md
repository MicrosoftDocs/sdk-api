---
UID: NS:projectedfslib.PRJ_NOTIFICATION_MAPPING
title: PRJ_NOTIFICATION_MAPPING (projectedfslib.h)
description: Describes a notification mapping, which is a pairing between a directory (referred to as a &quot;notification root&quot;) and a set of notifications, expressed as a bit mask.
helpviewer_keywords: ["PRJ_NOTIFICATION_MAPPING","PRJ_NOTIFICATION_MAPPING structure","ProjFS.prj_notification_mapping","projectedfslib/PRJ_NOTIFICATION_MAPPING"]
old-location: projfs\prj_notification_mapping.htm
tech.root: ProjFS
ms.assetid: 758E1ADB-8C16-46D9-B796-57C0B875790D
ms.date: 12/05/2018
ms.keywords: PRJ_NOTIFICATION_MAPPING, PRJ_NOTIFICATION_MAPPING structure, ProjFS.prj_notification_mapping, projectedfslib/PRJ_NOTIFICATION_MAPPING
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: PRJ_NOTIFICATION_MAPPING
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_NOTIFICATION_MAPPING
 - projectedfslib/PRJ_NOTIFICATION_MAPPING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_NOTIFICATION_MAPPING
---

# PRJ_NOTIFICATION_MAPPING structure


## -description

Describes a notification mapping, which is a pairing between a directory (referred to as a "notification root") and a set of notifications, expressed as a bit mask.

## -struct-fields

### -field NotificationBitMask

A bit mask representing a set of notifications.

### -field NotificationRoot

The directory that the notification mapping is paired to.

## -remarks

PRJ_NOTIFICATION_MAPPING describes a "notification mapping", which is a pairing between a directory (referred to as a "notification root") and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants. A notification mapping can also be established for a single file. 


The provider puts an array of zero or more PRJ_NOTIFICATION_MAPPING structures in the NotificationMappings member of the options parameter of PrjStartVirtualizing to configure notifications for the virtualization root. 


If the provider does not specify any notification mappings, ProjFS will default to sending the notifications PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, and PRJ_NOTIFICATION_FILE_OVERWRITTEN for all files and directories in the virtualization instance. 


The directory or file is specified relative to the virtualization root, with an empty string representing the virtualization root itself. 


If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth. Notification mappings at deeper levels override higher-level ones for their descendants.

