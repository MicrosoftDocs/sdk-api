---
UID: NS:ddrawint.DD_PALETTECALLBACKS
title: DD_PALETTECALLBACKS
author: windows-sdk-content
description: The DD_PALETTECALLBACKS structure contains entry pointers to the DirectDraw palette callback functions that a device driver supports.
old-location: display\dd_palettecallbacks.htm
tech.root: display
ms.assetid: 742b03b0-f729-489c-a87f-b8eb404b6290
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PDD_PALETTECALLBACKS, DD_PALETTECALLBACKS, DD_PALETTECALLBACKS structure [Display Devices], PDD_PALETTECALLBACKS, PDD_PALETTECALLBACKS structure pointer [Display Devices], ddrawint/DD_PALETTECALLBACKS, ddrawint/PDD_PALETTECALLBACKS, ddstrcts_def94357-6d48-46e6-848a-ef85f13de99e.xml, display.dd_palettecallbacks"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_PALETTECALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_PALETTECALLBACKS
req.redist: 
---

# DD_PALETTECALLBACKS structure


## -description


The DD_PALETTECALLBACKS structure contains entry pointers to the DirectDraw palette callback functions that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_PALETTECALLBACKS structure.


### -field dwFlags

Indicates what DirectDrawPalette callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_PALCB32_DESTROYPALETTE</dt>
<dt>DDHAL_PALCB32_SETENTRIES</dt>
</dl>



### -field DestroyPalette

Points to the driver-supplied <a href="https://msdn.microsoft.com/b44936fd-0052-4f54-9e97-1664c381c697">DdDestroyPalette</a> palette callback.


### -field SetEntries

Points to the driver-supplied <a href="https://msdn.microsoft.com/41b0b433-288d-4d7b-b961-2789b2540761">DdSetEntries</a> palette callback.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver initializes this structure in <a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a>.




## -see-also




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/b44936fd-0052-4f54-9e97-1664c381c697">DdDestroyPalette</a>



<a href="https://msdn.microsoft.com/41b0b433-288d-4d7b-b961-2789b2540761">DdSetEntries</a>



<a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a>
 

 

