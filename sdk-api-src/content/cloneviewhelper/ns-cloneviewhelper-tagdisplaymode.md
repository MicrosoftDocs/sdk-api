---
UID: NS:cloneviewhelper.tagDisplayMode
title: tagDisplayMode
author: windows-driver-content
description: The DisplayMode structure describes a display device.
old-location: display\displaymode.htm
old-project: display
ms.assetid: dc189bb6-e2c4-422c-8350-4c1632439478
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: DisplayMode, DisplayMode structure [Display Devices], TMM_Ref_37fe6fb5-e095-4bc7-8d92-a4d305bbadcb.xml, cloneviewhelper/DisplayMode, display.displaymode, tagDisplayMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DisplayMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	cloneviewhelper.h
api_name:
-	DisplayMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagDisplayMode structure


## -description


The DisplayMode structure describes a display device. 


## -struct-fields




### -field DeviceName

A single wide-character string that contains the name of the display device. 


### -field devMode

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552837">DEVMODEW</a> structure that contains characteristics of the display device. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552837">DEVMODEW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554039">DisplayModes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568176">IViewHelper::SetConfiguration</a>
 

 

