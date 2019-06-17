---
UID: NS:winsync._SYNC_TIME
title: SYNC_TIME (winsync.h)
author: windows-sdk-content
description: Represents a date-and-time value.
old-location: winsync\sync_time.htm
tech.root: winsync
ms.assetid: f5e0df02-d016-4eae-9b9b-bfd754ade126
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SYNC_TIME, SYNC_TIME structure [Windows Sync], winsync.sync_time, winsync/SYNC_TIME
ms.topic: struct
f1_keywords: ["winsync/SYNC_TIME"]
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winsync.h
api_name:
 - SYNC_TIME
product: Windows
targetos: Windows
req.typenames: SYNC_TIME
req.redist: 
ms.custom: 19H1
---

# SYNC_TIME structure


## -description


Represents a date-and-time value.


## -struct-fields




### -field dwDate

The date portion of the value.


### -field dwTime

The time portion of the value.


## -remarks



This structure is a packed date-and-time value that can store years between 1601 and 67136 and times that are accurate to the millisecond.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-structures">Windows Sync Structures</a>
 

 

