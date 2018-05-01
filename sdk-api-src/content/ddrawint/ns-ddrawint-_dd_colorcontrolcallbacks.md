---
UID: NS:ddrawint._DD_COLORCONTROLCALLBACKS
title: "_DD_COLORCONTROLCALLBACKS"
author: windows-driver-content
description: The DD_COLORCONTROLCALLBACKS structure contains an entry pointer to the Microsoft DirectDraw color control callback that a device driver supports.
old-location: display\dd_colorcontrolcallbacks.htm
old-project: display
ms.assetid: fcf0e136-a7cc-4bb3-8af4-2478d4a2c055
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*PDD_COLORCONTROLCALLBACKS, DD_COLORCONTROLCALLBACKS, DD_COLORCONTROLCALLBACKS structure [Display Devices], PDD_COLORCONTROLCALLBACKS, PDD_COLORCONTROLCALLBACKS structure pointer [Display Devices], _DD_COLORCONTROLCALLBACKS, ddrawint/DD_COLORCONTROLCALLBACKS, ddrawint/PDD_COLORCONTROLCALLBACKS, ddstrcts_2e14797b-2bd8-4107-8085-60f8b5838bda.xml, display.dd_colorcontrolcallbacks"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.typenames: DD_COLORCONTROLCALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_COLORCONTROLCALLBACKS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_COLORCONTROLCALLBACKS structure


## -description


The DD_COLORCONTROLCALLBACKS structure contains an entry pointer to the Microsoft DirectDraw color control callback that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_COLORCONTROLCALLBACKS structure.


### -field dwFlags

Indicates whether the device supports the color control callback identified by <b>ColorControl</b>. The driver should set this member to be DDHAL_COLOR_COLORCONTROL when it implements the color control callback.


### -field ColorControl

Points to the driver-supplied <a href="https://msdn.microsoft.com/626fdd37-bebb-47b7-9899-7cf0dc2bd1ba">DdControlColor</a> callback.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function is called with the GUID_ColorControlCallbacks GUID.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550485">DD_CALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551633">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551657">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551660">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551673">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551758">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/626fdd37-bebb-47b7-9899-7cf0dc2bd1ba">DdControlColor</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

