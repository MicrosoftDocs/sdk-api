---
UID: NS:cloneviewhelper.tagDisplayModes
title: DisplayModes (cloneviewhelper.h)
description: The DisplayModes structure contains a list of display modes.
helpviewer_keywords: ["DisplayModes","DisplayModes structure [Display Devices]","TMM_Ref_e94cf92c-8b36-4643-a34d-8e90faef7e72.xml","cloneviewhelper/DisplayModes","display.displaymodes"]
old-location: display\displaymodes.htm
tech.root: display
ms.assetid: 0add7a43-571f-4854-b019-d3601f915d48
ms.date: 12/05/2018
ms.keywords: DisplayModes, DisplayModes structure [Display Devices], TMM_Ref_e94cf92c-8b36-4643-a34d-8e90faef7e72.xml, cloneviewhelper/DisplayModes, display.displaymodes
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
req.typenames: DisplayModes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDisplayModes
 - cloneviewhelper/tagDisplayModes
 - DisplayModes
 - cloneviewhelper/DisplayModes
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
 - DisplayModes
---

# DisplayModes structure


## -description

The DisplayModes structure contains a list of display modes.

## -struct-fields

### -field numDisplayModes

The number of display modes in the array that the <b>displayMode</b> member specifies.

### -field displayMode

An array of <a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-displaymode">DisplayMode</a> structures that describe characteristics of display devices.

## -see-also

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-displaymode">DisplayMode</a>



<a href="/previous-versions/windows/hardware/drivers/ff568176(v=vs.85)">IViewHelper::SetConfiguration</a>