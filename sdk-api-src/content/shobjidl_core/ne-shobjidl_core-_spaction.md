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

# _SPACTION enumeration


## -description


Describes an action being performed that requires progress to be shown to the user using an <a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a> interface.


## -enum-fields




### -field SPACTION_NONE

No action is being performed.


### -field SPACTION_MOVING

Files are being moved.


### -field SPACTION_COPYING

Files are being copied.


### -field SPACTION_RECYCLING

Files are being deleted.


### -field SPACTION_APPLYINGATTRIBS

A set of attributes are being applied to files.


### -field SPACTION_DOWNLOADING

A file is being downloaded from a remote source.


### -field SPACTION_SEARCHING_INTERNET

An Internet search is being performed.


### -field SPACTION_CALCULATING

A calculation is being performed.


### -field SPACTION_UPLOADING

A file is being uploaded to a remote source.


### -field SPACTION_SEARCHING_FILES

A local search is being performed.


### -field SPACTION_DELETING

<b>Windows Vista and later</b>. A deletion is being performed.


### -field SPACTION_RENAMING

<b>Windows Vista and later</b>. A renaming action is being performed.


### -field SPACTION_FORMATTING

<b>Windows Vista and later</b>. A formatting action is being performed.


### -field SPACTION_COPY_MOVING

<b>Windows 7 and later</b>. A copy or move action is being performed.


## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>
 

 

