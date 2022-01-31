---
UID: NE:wmpservices.WMPPlugin_Caps
title: WMPPlugin_Caps (wmpservices.h)
description: The WMPPlugin_Caps enumeration type signals whether the plug-in can convert between input and output formats.
helpviewer_keywords: ["WMPPlugin_Caps","WMPPlugin_Caps enumeration [Windows Media Player]","WMPPlugin_CapsDSP","WMPPlugin_Caps_CannotConvertFormats","wmp.wmpplugin_caps","wmpservices/WMPPlugin_Caps","wmpservices/WMPPlugin_Caps_CannotConvertFormats"]
old-location: wmp\wmpplugin_caps.htm
tech.root: WMP
ms.assetid: 0f6cad76-7583-4272-88d7-25a121a0c2b9
ms.date: 12/05/2018
ms.keywords: WMPPlugin_Caps, WMPPlugin_Caps enumeration [Windows Media Player], WMPPlugin_CapsDSP, WMPPlugin_Caps_CannotConvertFormats, wmp.wmpplugin_caps, wmpservices/WMPPlugin_Caps, wmpservices/WMPPlugin_Caps_CannotConvertFormats
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.typenames: WMPPlugin_Caps
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPPlugin_Caps
 - wmpservices/WMPPlugin_Caps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmpservices.h
api_name:
 - WMPPlugin_Caps
---

# WMPPlugin_Caps enumeration


## -description

The <b>WMPPlugin_Caps</b> enumeration type signals whether the plug-in can convert between input and output formats.

## -enum-fields

### -field WMPPlugin_Caps_CannotConvertFormats:1

The plug-in requires that the input format and output format be the same.

## -remarks

When <b>IWMPPlugin::GetCaps</b> returns <b>WMPPlugin_Caps_CannotConvertFormats</b>, Windows Media Player handles any necessary format conversion.

## -see-also

<a href="/windows/desktop/WMP/dsp-plug-in-enumeration-types">DSP Plug-in Enumeration Types</a>



<a href="/previous-versions/aa391071(v=vs.85)">IWMPPlugin::GetCaps</a>
