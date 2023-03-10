---
UID: NS:cloneviewhelper.tagDisplayMode
title: DisplayMode (cloneviewhelper.h)
description: The DisplayMode structure describes a display device.
helpviewer_keywords: ["DisplayMode","DisplayMode structure [Display Devices]","TMM_Ref_37fe6fb5-e095-4bc7-8d92-a4d305bbadcb.xml","cloneviewhelper/DisplayMode","display.displaymode"]
old-location: display\displaymode.htm
tech.root: display
ms.assetid: dc189bb6-e2c4-422c-8350-4c1632439478
ms.date: 12/05/2018
ms.keywords: DisplayMode, DisplayMode structure [Display Devices], TMM_Ref_37fe6fb5-e095-4bc7-8d92-a4d305bbadcb.xml, cloneviewhelper/DisplayMode, display.displaymode
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
req.typenames: DisplayMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDisplayMode
 - cloneviewhelper/tagDisplayMode
 - DisplayMode
 - cloneviewhelper/DisplayMode
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
 - DisplayMode
---

# DisplayMode structure


## -description

The DisplayMode structure describes a display device.

## -struct-fields

### -field DeviceName

A single wide-character string that contains the name of the display device.

### -field devMode

A <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODEW</a> structure that contains characteristics of the display device.

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODEW</a>



<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-displaymodes">DisplayModes</a>



<a href="/previous-versions/windows/hardware/drivers/ff568176(v=vs.85)">IViewHelper::SetConfiguration</a>