---
UID: NF:winddi.EngControlSprites
title: EngControlSprites function (winddi.h)
description: The EngControlSprites function tears down or redraws sprites on the specified WNDOBJ area.
helpviewer_keywords: ["EngControlSprites","EngControlSprites function [Display Devices]","display.engcontrolsprites","gdifncs_b7312326-43ba-4c8b-bb23-db2ecf2d6f6e.xml","winddi/EngControlSprites"]
old-location: display\engcontrolsprites.htm
tech.root: display
ms.assetid: 8de02019-6f58-4adc-9589-fdfbf4a062aa
ms.date: 12/05/2018
ms.keywords: EngControlSprites, EngControlSprites function [Display Devices], display.engcontrolsprites, gdifncs_b7312326-43ba-4c8b-bb23-db2ecf2d6f6e.xml, winddi/EngControlSprites
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngControlSprites
 - winddi/EngControlSprites
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngControlSprites
---

# EngControlSprites function


## -description

The <b>EngControlSprites</b> function tears down or redraws sprites on the specified <a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a> area.

## -parameters

### -param pwo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a> structure on which the sprites are being built or torn down.

### -param fl

This parameter can be one of the following values:





#### ECS_TEARDOWN

Requests that GDI tear down and remove the sprite effect of any sprite that overlaps the WNDOBJ area. In other words, GDI redraws the sprite with a neutralized effect so the sprite is not visible on the screen. GDI restores the area beneath the sprite by making immediate calls to <a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a>.



#### ECS_REDRAW

Requests that GDI redraw, restoring any sprites that overlap the WNDOBJ area. GDI redraws directly to the screen by making calls to <i>DrvCopyBits</i>.

## -returns

<b>EngControlSprites</b> returns <b>TRUE</b> upon successfully completing the requested operation; otherwise, it returns <b>FALSE</b>.

## -remarks

The invocation of ECS_TEARDOWN may be persistent. For example, the driver can call <b>EngControlSprites</b> once with ECS_TEARDOWN as soon as it has created the WNDOBJ, and no sprites will ever be drawn on top of the window.

The driver can call <b>EngControlSprites</b> with ECS_REDRAW numerous times without making intervening calls with ECS_TEARDOWN in order to force the repainting of a sprite at any time.

ECS_TEARDOWN always forces an immediate redraw of any sprites on top of the WNDOBJ area. GDI saves the bits beneath the sprites by calling <a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a> to copy them from the screen, and then composites the sprites onto the screen by calling <i>DrvCopyBits</i>. This can be used to allow sprites to be composited onto a back-buffer just before a swap-buffer command is sent to the hardware (through <a href="/windows/desktop/api/winddi/nf-winddi-drvswapbuffers">DrvSwapBuffers</a> or any other driver swap buffer mechanism). This permits seamless compositing of sprites, without flashing, when the window is double buffering.

ECS_TEARDOWN will never cause a WOC_SPRITE_NO_OVERLAP message to be sent, and likewise ECS_REDRAW will never cause a WOC_SPRITE_OVERLAP message to be sent.

<b>EngControlSprites</b> can be called even if no sprites currently overlap the WNDOBJ area.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatewnd">EngCreateWnd</a>



<a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a>