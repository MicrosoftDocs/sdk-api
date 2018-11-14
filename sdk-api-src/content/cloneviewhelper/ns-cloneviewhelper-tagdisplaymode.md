---
UID: NS:cloneviewhelper.tagDisplayMode
title: tagDisplayMode
author: windows-sdk-content
description: The DisplayMode structure describes a display device.
old-location: display\displaymode.htm
tech.root: display
ms.assetid: dc189bb6-e2c4-422c-8350-4c1632439478
ms.author: windowssdkdev
ms.date: 11/02/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cloneviewhelper.h
api_name:
 - DisplayMode
product: Windows
targetos: Windows
req.typenames: DisplayMode
req.redist: 
---

# tagDisplayMode structure


## -description


The DisplayMode structure describes a display device. 


## -struct-fields




### -field DeviceName

A single wide-character string that contains the name of the display device. 


### -field devMode

A <a href="https://msdn.microsoft.com/b2369876-9a79-40c8-8d27-c8b9d8e68e6b">DEVMODEW</a> structure that contains characteristics of the display device. 


## -see-also




<a href="https://msdn.microsoft.com/b2369876-9a79-40c8-8d27-c8b9d8e68e6b">DEVMODEW</a>



<a href="https://msdn.microsoft.com/0add7a43-571f-4854-b019-d3601f915d48">DisplayModes</a>



<a href="https://msdn.microsoft.com/8ec09950-afb6-43ff-8e05-4c801e49ba4b">IViewHelper::SetConfiguration</a>
 

 

