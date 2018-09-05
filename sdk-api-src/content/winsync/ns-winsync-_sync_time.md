---
UID: NS:winsync._SYNC_TIME
title: "_SYNC_TIME"
author: windows-sdk-content
description: Represents a date-and-time value.
old-location: winsync\sync_time.htm
old-project: winsync
ms.assetid: f5e0df02-d016-4eae-9b9b-bfd754ade126
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SYNC_TIME, SYNC_TIME structure [Windows Sync], _SYNC_TIME, winsync.sync_time, winsync/SYNC_TIME
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsync.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SYNC_TIME
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SYNC_TIME structure


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




<a href="https://msdn.microsoft.com/eed33384-f8bd-4a3a-8d04-b59c534f9114">Windows Sync Structures</a>
 

 

