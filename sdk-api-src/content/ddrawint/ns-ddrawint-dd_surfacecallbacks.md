---
UID: NS:ddrawint.DD_SURFACECALLBACKS
title: DD_SURFACECALLBACKS
author: windows-sdk-content
description: The DD_SURFACECALLBACKS structure contains entry pointers to the Microsoft DirectDraw surface callback functions that a device driver supports.
old-location: display\dd_surfacecallbacks.htm
tech.root: display
ms.assetid: a363446e-a9f7-4b32-acc2-c369d3dfe8f3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PDD_SURFACECALLBACKS, DD_SURFACECALLBACKS, DD_SURFACECALLBACKS structure [Display Devices], PDD_SURFACECALLBACKS, PDD_SURFACECALLBACKS structure pointer [Display Devices], ddrawint/DD_SURFACECALLBACKS, ddrawint/PDD_SURFACECALLBACKS, ddstrcts_868cb884-02fc-4df4-a3ec-1fde158e42b0.xml, display.dd_surfacecallbacks"
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
 - DD_SURFACECALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_SURFACECALLBACKS
req.redist: 
---

# DD_SURFACECALLBACKS structure


## -description


The DD_SURFACECALLBACKS structure contains entry pointers to the Microsoft DirectDraw surface callback functions that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of the DD_SURFACECALLBACKS structure. This member is unused by Microsoft Windows 2000 and later versions.


### -field dwFlags

Indicates which DirectDrawSurface callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_SURFCB32_DESTROYSURFACE</dt>
<dt>DDHAL_SURFCB32_FLIP</dt>
<dt>DDHAL_SURFCB32_SETCLIPLIST</dt>
<dt>DDHAL_SURFCB32_LOCK</dt>
<dt>DDHAL_SURFCB32_UNLOCK</dt>
<dt>DDHAL_SURFCB32_BLT</dt>
<dt>DDHAL_SURFCB32_SETCOLORKEY</dt>
<dt>DDHAL_SURFCB32_ADDATTACHEDSURFACE</dt>
<dt>DDHAL_SURFCB32_GETBLTSTATUS</dt>
<dt>DDHAL_SURFCB32_GETFLIPSTATUS</dt>
<dt>DDHAL_SURFCB32_UPDATEOVERLAY</dt>
<dt>DDHAL_SURFCB32_SETOVERLAYPOSITION</dt>
<dt>DDHAL_SURFCB32_SETPALETTE</dt>
</dl>



### -field DestroySurface

Points to the driver-supplied <a href="https://msdn.microsoft.com/90060863-02ef-49bf-820d-b3adffbc8f40">DdDestroySurface</a> surface callback.


### -field Flip

Points to the driver-supplied <a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a> surface callback.


### -field SetClipList

Points to the driver-supplied <a href="https://msdn.microsoft.com/library/Ff550300(v=VS.85).aspx">DdSetClipList</a> surface callback.


### -field Lock

Points to the driver-supplied <a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a> surface callback.


### -field Unlock

Points to the driver-supplied <a href="https://msdn.microsoft.com/dbb7b34c-5473-42b9-b16f-e71b9c3e1db8">DdUnlock</a> surface callback.


### -field Blt

Points to the driver-supplied <a href="https://msdn.microsoft.com/28e0c827-33f1-4b83-9f20-bbb66bc0e14a">DdBlt</a> surface callback.


### -field SetColorKey

Points to the driver-supplied <a href="https://msdn.microsoft.com/4b4ee889-15c8-4a7c-a9d8-adab27b271dd">DdSetColorKey</a> surface callback.


### -field AddAttachedSurface

Points to the driver-supplied <a href="https://msdn.microsoft.com/53f146e6-f521-4c95-b98b-0e8acb994c9d">DdAddAttachedSurface</a> surface callback.


### -field GetBltStatus

Points to the driver-supplied <a href="https://msdn.microsoft.com/77cce7a4-a0e6-48f7-933f-a216b13ddc93">DdGetBltStatus</a> surface callback.


### -field GetFlipStatus

Points to the driver-supplied <a href="https://msdn.microsoft.com/ec556891-e091-4c52-a155-cb6ba8011f71">DdGetFlipStatus</a> surface callback.


### -field UpdateOverlay

Points to the driver-supplied <a href="https://msdn.microsoft.com/e86b3b75-319a-4817-bcb1-59580c855ef9">DdUpdateOverlay</a> surface callback.


### -field SetOverlayPosition

Points to the driver-supplied <a href="https://msdn.microsoft.com/0bafdeea-d06d-4c25-9ee5-b7df23d7dd20">DdSetOverlayPosition</a> surface callback.


### -field reserved4

Reserved for system use and should be ignored by the driver.


### -field SetPalette

Points to the driver-supplied <a href="https://msdn.microsoft.com/745b30f0-3d2f-4894-8991-6b7d511f8493">DdSetPalette</a> surface callback.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver initializes this structure in <a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a>.




## -see-also




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a>
 

 

