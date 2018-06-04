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

# _VSS_SNAPSHOT_COMPATIBILITY enumeration


## -description


The <b>VSS_SNAPSHOT_COMPATIBILITY</b> enumeration 
    indicates which volume control or file I/O operations are disabled for the volume that has been shadow copied.


## -enum-fields




### -field VSS_SC_DISABLE_DEFRAG

The provider managing the shadow copies for a specified volume does not support defragmentation operations 
      on that volume.


### -field VSS_SC_DISABLE_CONTENTINDEX

The provider managing the shadow copies for a specified volume does not support content index operations on 
      that volume.

