---
UID: NE:mmc._MMC_CONTROL_TYPE
title: MMC_CONTROL_TYPE (mmc.h)
description: The MMC_CONTROL_TYPE enumeration defines the kinds of controls that can appear in the control bar. The values can be used in the nType parameter of the IControlbar::Attach and IControlbar::Create methods.
helpviewer_keywords: ["COMBOBOXBAR","MENUBUTTON","MMC_CONTROL_TYPE","MMC_CONTROL_TYPE enumeration [MMC]","TOOLBAR","_slate_mmc_control_type","mmc.mmc_control_type","mmc/COMBOBOXBAR","mmc/MENUBUTTON","mmc/MMC_CONTROL_TYPE","mmc/TOOLBAR"]
old-location: mmc\mmc_control_type.htm
tech.root: mmc
ms.assetid: f4f64769-a3d0-46eb-8520-a6cb7237d007
ms.date: 12/05/2018
ms.keywords: COMBOBOXBAR, MENUBUTTON, MMC_CONTROL_TYPE, MMC_CONTROL_TYPE enumeration [MMC], TOOLBAR, _slate_mmc_control_type, mmc.mmc_control_type, mmc/COMBOBOXBAR, mmc/MENUBUTTON, mmc/MMC_CONTROL_TYPE, mmc/TOOLBAR
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: MMC_CONTROL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_CONTROL_TYPE
 - mmc/_MMC_CONTROL_TYPE
 - MMC_CONTROL_TYPE
 - mmc/MMC_CONTROL_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_CONTROL_TYPE
---

# MMC_CONTROL_TYPE enumeration


## -description

The 
MMC_CONTROL_TYPE enumeration defines the kinds of controls that can appear in the control bar. The values can be used in the nType parameter of the 
<a href="/windows/desktop/api/mmc/nf-mmc-icontrolbar-attach">IControlbar::Attach</a> and 
<a href="/windows/desktop/api/mmc/nf-mmc-icontrolbar-create">IControlbar::Create</a> methods.

## -enum-fields

### -field TOOLBAR:0

The control to be associated with the control bar is a toolbar.

### -field MENUBUTTON

The control is a drop-down menu. This is a standard Win32 menu button.

### -field COMBOBOXBAR

Not implemented at this time. This is a standard Win32 combo box.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-icontrolbar-attach">IControlbar::Attach</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icontrolbar-create">IControlbar::Create</a>
