---
UID: NS:cloneviewhelper.tagDisplayModes
title: tagDisplayModes
author: windows-driver-content
description: The DisplayModes structure contains a list of display modes.
old-location: display\displaymodes.htm
old-project: display
ms.assetid: 0add7a43-571f-4854-b019-d3601f915d48
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DisplayModes, DisplayModes structure [Display Devices], TMM_Ref_e94cf92c-8b36-4643-a34d-8e90faef7e72.xml, cloneviewhelper/DisplayModes, display.displaymodes, tagDisplayModes
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
req.typenames: DisplayModes
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	cloneviewhelper.h
api_name:
-	DisplayModes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagDisplayModes structure


## -description


The DisplayModes structure contains a list of display modes. 


## -struct-fields




### -field numDisplayModes

The number of display modes in the array that the <b>displayMode</b> member specifies. 


### -field displayMode

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff554037">DisplayMode</a> structures that describe characteristics of display devices. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff554037">DisplayMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568176">IViewHelper::SetConfiguration</a>
 

 

