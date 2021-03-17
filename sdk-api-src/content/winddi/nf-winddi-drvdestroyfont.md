---
UID: NF:winddi.DrvDestroyFont
title: DrvDestroyFont function (winddi.h)
description: The DrvDestroyFont function notifies the driver that a font realization is no longer needed and that the driver can now free any associated data structures it has allocated.
helpviewer_keywords: ["DrvDestroyFont","DrvDestroyFont function [Display Devices]","ddifncs_a73e0b14-897a-423d-a9db-8c4ba831a36b.xml","display.drvdestroyfont","winddi/DrvDestroyFont"]
old-location: display\drvdestroyfont.htm
tech.root: display
ms.assetid: aee3efbc-715d-42f2-a718-00057720175a
ms.date: 12/05/2018
ms.keywords: DrvDestroyFont, DrvDestroyFont function [Display Devices], ddifncs_a73e0b14-897a-423d-a9db-8c4ba831a36b.xml, display.drvdestroyfont, winddi/DrvDestroyFont
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvDestroyFont
 - winddi/DrvDestroyFont
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDestroyFont
---

# DrvDestroyFont function


## -description

The <b>DrvDestroyFont</b> function notifies the driver that a font realization is no longer needed and that the driver can now free any associated data structures it has allocated.

## -parameters

### -param pfo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure that identifies the font instance.

## -remarks

The <b>DrvDestroyFont</b> function is called only in font drivers and kernel-mode printer drivers. 

If the DEVICE_FONTTYPE flag is set in the <b>flFontType</b> member of the FONTOBJ structure, the driver should release any resources or memory identified with both the <b>pvConsumer</b> and <b>pvProducer</b> members of FONTOBJ. Otherwise, it should release only memory and resources identified with <b>pvConsumer</b>.

The driver must reset the <b>pvConsumer</b> and <b>pvProducer</b> members to <b>NULL</b> if it uses them.

GDI calls <b>DrvDestroyFont</b> once for the font producer and once again for the font consumer.

GDI guarantees that <b>DrvDestroyFont</b> and <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a> never overlap; consequently, the driver can rely on cached information while processing a <b>DrvTextOut</b> call.

This function must be implemented if the font driver or kernel-mode printer driver allocates resources when it realizes fonts.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>