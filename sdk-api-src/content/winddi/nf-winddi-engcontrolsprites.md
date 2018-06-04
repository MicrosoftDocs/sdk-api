---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# EngControlSprites function


## -description


The <b>EngControlSprites</b> function tears down or redraws sprites on the specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> area.


## -parameters




### -param pwo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure on which the sprites are being built or torn down.


### -param fl

This parameter can be one of the following values:





#### ECS_TEARDOWN

Requests that GDI tear down and remove the sprite effect of any sprite that overlaps the WNDOBJ area. In other words, GDI redraws the sprite with a neutralized effect so the sprite is not visible on the screen. GDI restores the area beneath the sprite by making immediate calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556182">DrvCopyBits</a>.



#### ECS_REDRAW

Requests that GDI redraw, restoring any sprites that overlap the WNDOBJ area. GDI redraws directly to the screen by making calls to <i>DrvCopyBits</i>.


## -returns



<b>EngControlSprites</b> returns <b>TRUE</b> upon successfully completing the requested operation; otherwise, it returns <b>FALSE</b>.




## -remarks



The invocation of ECS_TEARDOWN may be persistent. For example, the driver can call <b>EngControlSprites</b> once with ECS_TEARDOWN as soon as it has created the WNDOBJ, and no sprites will ever be drawn on top of the window.

The driver can call <b>EngControlSprites</b> with ECS_REDRAW numerous times without making intervening calls with ECS_TEARDOWN in order to force the repainting of a sprite at any time.

ECS_TEARDOWN always forces an immediate redraw of any sprites on top of the WNDOBJ area. GDI saves the bits beneath the sprites by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff556182">DrvCopyBits</a> to copy them from the screen, and then composites the sprites onto the screen by calling <i>DrvCopyBits</i>. This can be used to allow sprites to be composited onto a back-buffer just before a swap-buffer command is sent to the hardware (through <a href="https://msdn.microsoft.com/library/windows/hardware/ff556322">DrvSwapBuffers</a> or any other driver swap buffer mechanism). This permits seamless compositing of sprites, without flashing, when the window is double buffering.

ECS_TEARDOWN will never cause a WOC_SPRITE_NO_OVERLAP message to be sent, and likewise ECS_REDRAW will never cause a WOC_SPRITE_OVERLAP message to be sent.

<b>EngControlSprites</b> can be called even if no sprites currently overlap the WNDOBJ area.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a>
 

 

