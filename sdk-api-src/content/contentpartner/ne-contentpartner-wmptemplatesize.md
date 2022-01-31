---
UID: NE:contentpartner.WMPTemplateSize
title: WMPTemplateSize (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The WMPTemplateSize enumeration represents HTML template sizes.
helpviewer_keywords: ["WMPTemplateSize","WMPTemplateSize enumeration [Windows Media Player]","contentpartner/WMPTemplateSize","contentpartner/wmptsLarge","contentpartner/wmptsMedium","contentpartner/wmptsSmall","enumeration [Windows Media Player]","wmp.wmptemplatesize","wmptsLarge","wmptsMedium","wmptsSmall"]
old-location: wmp\wmptemplatesize.htm
tech.root: WMP
ms.assetid: c63185a7-b2a4-4c3d-b455-220e1954a31a
ms.date: 12/05/2018
ms.keywords: WMPTemplateSize, WMPTemplateSize enumeration [Windows Media Player], contentpartner/WMPTemplateSize, contentpartner/wmptsLarge, contentpartner/wmptsMedium, contentpartner/wmptsSmall, enumeration [Windows Media Player], wmp.wmptemplatesize, wmptsLarge, wmptsMedium, wmptsSmall
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
req.typenames: WMPTemplateSize
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPTemplateSize
 - contentpartner/WMPTemplateSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPTemplateSize
---

# WMPTemplateSize enumeration


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPTemplateSize</b> enumeration represents HTML template sizes.

## -enum-fields

### -field wmptsSmall:0

Small template; height is fixed at 100 pixels.

### -field wmptsMedium

Medium template; height is fixed at 250 pixels.

### -field wmptsLarge

Large template. Windows Media Player allocates as much room as possible while allowing space for the list control to display a single row of items.

## -see-also

<a href="/windows/desktop/WMP/enumerations-for-type-1-online-stores">Enumerations for Type 1 Online Stores</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate">IWMPContentPartner::GetTemplate</a>
