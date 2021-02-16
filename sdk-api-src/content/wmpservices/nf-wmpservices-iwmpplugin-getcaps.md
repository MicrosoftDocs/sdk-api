---
UID: NF:wmpservices.IWMPPlugin.GetCaps
title: IWMPPlugin::GetCaps (wmpservices.h)
description: The IWMPPlugin::GetCaps method returns a flag that specifies whether the plug-in can convert between an input format and an output format.
helpviewer_keywords: ["GetCaps","GetCaps method [Windows Media Player]","GetCaps method [Windows Media Player]","IWMPPlugin interface","IWMPPlugin interface [Windows Media Player]","GetCaps method","IWMPPlugin.GetCaps","IWMPPlugin::GetCaps","IWMPPluginGetCapsDSP","wmp.iwmpplugin_getcaps","wmpservices/IWMPPlugin::GetCaps"]
old-location: wmp\iwmpplugin_getcaps.htm
tech.root: WMP
ms.assetid: f8b38453-47a3-4330-88f8-8d8993089f75
ms.date: 12/05/2018
ms.keywords: GetCaps, GetCaps method [Windows Media Player], GetCaps method [Windows Media Player],IWMPPlugin interface, IWMPPlugin interface [Windows Media Player],GetCaps method, IWMPPlugin.GetCaps, IWMPPlugin::GetCaps, IWMPPluginGetCapsDSP, wmp.iwmpplugin_getcaps, wmpservices/IWMPPlugin::GetCaps
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPPlugin::GetCaps
 - wmpservices/IWMPPlugin::GetCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPPlugin.GetCaps
---

# IWMPPlugin::GetCaps


## -description

The <b>IWMPPlugin::GetCaps</b> method returns a flag that specifies whether the plug-in can convert between an input format and an output format.

## -parameters

### -param pdwFlags [out]

Pointer to a variable that specifies whether the plug-in can convert formats. The specified value is a bitwise combination of zero or more flags from the <b>WMPPlugin_Caps</b> enumeration.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

There are currently two possible [out] values that the plug-in may specify: zero to indicate that the plug-in can convert formats, or <b>WMPPlugin_Caps_CannotConvertFormats</b>, which forces Windows Media Player to handle any necessary format conversion.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>



<a href="/windows/desktop/api/wmpservices/ne-wmpservices-wmpplugin_caps">WMPPlugin_Caps</a>