---
UID: NE:vss._VSS_SNAPSHOT_COMPATIBILITY
title: "_VSS_SNAPSHOT_COMPATIBILITY"
author: windows-sdk-content
description: The VSS_SNAPSHOT_COMPATIBILITY enumeration indicates which volume control or file I/O operations are disabled for the volume that has been shadow copied.
old-location: base\vss_snapshot_compatibility.htm
old-project: VSS
ms.assetid: 105d7bd6-0e95-4803-ae39-f03af40daa8e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: VSS_SC_DISABLE_CONTENTINDEX, VSS_SC_DISABLE_DEFRAG, VSS_SNAPSHOT_COMPATIBILITY, VSS_SNAPSHOT_COMPATIBILITY enumeration [VSS], _VSS_SNAPSHOT_COMPATIBILITY, _win32_vss_snapshot_compatibility, base.vss_snapshot_compatibility, vss/VSS_SC_DISABLE_CONTENTINDEX, vss/VSS_SC_DISABLE_DEFRAG, vss/VSS_SNAPSHOT_COMPATIBILITY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VSS_SNAPSHOT_COMPATIBILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_SNAPSHOT_COMPATIBILITY
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
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

