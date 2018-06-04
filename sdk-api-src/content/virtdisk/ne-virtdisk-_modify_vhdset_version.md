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

# _MODIFY_VHDSET_VERSION enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains the version of the <a href="https://msdn.microsoft.com/558323D6-2D97-40C8-9CAF-E97604D2F742">MODIFY_VHDSET_PARAMETERS</a> structure to use in calls to virtual disk functions.


## -enum-fields




### -field MODIFY_VHDSET_UNSPECIFIED

Not Supported.


### -field MODIFY_VHDSET_SNAPSHOT_PATH

The <b>SnapshotPath</b> member structure will be used.


### -field MODIFY_VHDSET_REMOVE_SNAPSHOT

The <b>SnapshotId</b> member structure will be used.


### -field MODIFY_VHDSET_DEFAULT_SNAPSHOT_PATH

The <b>DefaultFilePath</b> member structure will be used

