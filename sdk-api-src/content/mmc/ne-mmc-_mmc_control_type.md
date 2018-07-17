---
UID: NE:mmc._MMC_CONTROL_TYPE
title: "_MMC_CONTROL_TYPE"
author: windows-sdk-content
description: The MMC_CONTROL_TYPE enumeration defines the kinds of controls that can appear in the control bar. The values can be used in the nType parameter of the IControlbar::Attach and IControlbar::Create methods.
old-location: mmc\mmc_control_type.htm
old-project: mmc
ms.assetid: f4f64769-a3d0-46eb-8520-a6cb7237d007
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: COMBOBOXBAR, MENUBUTTON, MMC_CONTROL_TYPE, MMC_CONTROL_TYPE enumeration [MMC], TOOLBAR, _MMC_CONTROL_TYPE, _slate_mmc_control_type, mmc.mmc_control_type, mmc/COMBOBOXBAR, mmc/MENUBUTTON, mmc/MMC_CONTROL_TYPE, mmc/TOOLBAR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MMC_CONTROL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_CONTROL_TYPE
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_CONTROL_TYPE enumeration


## -description


The 
MMC_CONTROL_TYPE enumeration defines the kinds of controls that can appear in the control bar. The values can be used in the nType parameter of the 
<a href="https://msdn.microsoft.com/60ed8f9a-d5ad-4a68-8019-6887104c9b2a">IControlbar::Attach</a> and 
<a href="https://msdn.microsoft.com/2ce92539-f5dc-44c3-94e5-253fc9995932">IControlbar::Create</a> methods.


## -enum-fields




### -field TOOLBAR

The control to be associated with the control bar is a toolbar.


### -field MENUBUTTON

The control is a drop-down menu. This is a standard Win32 menu button.


### -field COMBOBOXBAR

Not implemented at this time. This is a standard Win32 combo box.


## -see-also




<a href="https://msdn.microsoft.com/60ed8f9a-d5ad-4a68-8019-6887104c9b2a">IControlbar::Attach</a>



<a href="https://msdn.microsoft.com/2ce92539-f5dc-44c3-94e5-253fc9995932">IControlbar::Create</a>
 

 

