---
UID: NS:cloneviewhelper.tagSources
title: Sources (cloneviewhelper.h)
description: The Sources structure contains a Video Present Network (VidPN) topology.
helpviewer_keywords: ["Sources","Sources structure [Display Devices]","TMM_Ref_e15dfa1e-b8f8-464e-b683-c968113fbf64.xml","cloneviewhelper/Sources","display.sources"]
old-location: display\sources.htm
tech.root: display
ms.assetid: 5fbb12bc-d6e0-4cb7-b9d7-4e28ad85eca2
ms.date: 12/05/2018
ms.keywords: Sources, Sources structure [Display Devices], TMM_Ref_e15dfa1e-b8f8-464e-b683-c968113fbf64.xml, cloneviewhelper/Sources, display.sources
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: Sources
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSources
 - cloneviewhelper/tagSources
 - Sources
 - cloneviewhelper/Sources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cloneviewhelper.h
api_name:
 - Sources
---

# Sources structure


## -description

The Sources structure contains a Video Present Network (VidPN) topology.

## -struct-fields

### -field sourceId

The source identifier for the video present source in the VidPN topology.

### -field numTargets

The number of video present targets in the array that the <b>aTargets</b> member specifies, which is the number of video present targets in the VidPN topology.

### -field aTargets

An array of identifiers for the video present targets in the VidPN topology.

## -see-also

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-adapter">Adapter</a>



<a href="/previous-versions/windows/hardware/drivers/ff568176(v=vs.85)">IViewHelper::SetConfiguration</a>