---
UID: NE:shobjidl_core.PLACEHOLDER_STATES
title: PLACEHOLDER_STATES
author: windows-sdk-content
description: Specifies the states that a placeholder file can have. Retrieve this value through the System.FilePlaceholderStatus (PKEY_FilePlaceholderStatus) property.
old-location: properties\PLACEHOLDER_STATES.htm
tech.root: properties
ms.assetid: BF4E0A9F-CD78-4D29-AD0C-7DF14AE88447
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PLACEHOLDER_STATES, PLACEHOLDER_STATES enumeration [Windows Properties], PS_ALL, PS_CREATE_FILE_ACCESSIBLE, PS_FULL_PRIMARY_STREAM_AVAILABLE, PS_MARKED_FOR_OFFLINE_AVAILABILITY, PS_NONE, properties.PLACEHOLDER_STATES, shobjidl_core/PLACEHOLDER_STATES, shobjidl_core/PS_ALL, shobjidl_core/PS_CREATE_FILE_ACCESSIBLE, shobjidl_core/PS_FULL_PRIMARY_STREAM_AVAILABLE, shobjidl_core/PS_MARKED_FOR_OFFLINE_AVAILABILITY, shobjidl_core/PS_NONE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl_core.h
api_name:
 - PLACEHOLDER_STATES
product: Windows
targetos: Windows
req.typenames: PLACEHOLDER_STATES
req.redist: 
---

# PLACEHOLDER_STATES enumeration


## -description


Specifies the states that a placeholder file can have. Retrieve this value through the System.FilePlaceholderStatus (PKEY_FilePlaceholderStatus) property.


## -enum-fields




### -field PS_NONE

None of the other states apply at this time.


### -field PS_MARKED_FOR_OFFLINE_AVAILABILITY

May already be or eventually will be available offline.


### -field PS_FULL_PRIMARY_STREAM_AVAILABLE

The primary stream has been made fully available.


### -field PS_CREATE_FILE_ACCESSIBLE

The file is accessible through a call to the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, without requesting the opening of reparse points.


### -field PS_CLOUDFILE_PLACEHOLDER


### -field PS_DEFAULT


### -field PS_ALL

A bitmask value for all valid PLACEHOLDER_STATES flags.

