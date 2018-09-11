---
UID: NE:wmpservices.WMPPlugin_Caps
title: WMPPlugin_Caps
author: windows-sdk-content
description: The WMPPlugin_Caps enumeration type signals whether the plug-in can convert between input and output formats.
old-location: wmp\wmpplugin_caps.htm
tech.root: WMP
ms.assetid: 0f6cad76-7583-4272-88d7-25a121a0c2b9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WMPPlugin_Caps, WMPPlugin_Caps enumeration [Windows Media Player], WMPPlugin_CapsDSP, WMPPlugin_Caps_CannotConvertFormats, wmp.wmpplugin_caps, wmpservices/WMPPlugin_Caps, wmpservices/WMPPlugin_Caps_CannotConvertFormats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmpservices.h
api_name:
 - WMPPlugin_Caps
product: Windows
targetos: Windows
req.typenames: WMPPlugin_Caps
req.redist: 
---

# WMPPlugin_Caps enumeration


## -description



The <b>WMPPlugin_Caps</b> enumeration type signals whether the plug-in can convert between input and output formats.




## -enum-fields




### -field WMPPlugin_Caps_CannotConvertFormats

The plug-in requires that the input format and output format be the same.


## -remarks



When <b>IWMPPlugin::GetCaps</b> returns <b>WMPPlugin_Caps_CannotConvertFormats</b>, Windows Media Player handles any necessary format conversion.




## -see-also




<a href="https://msdn.microsoft.com/7b1b74e6-19de-450a-be89-41277c1cb823">DSP Plug-in Enumeration Types</a>



<a href="https://msdn.microsoft.com/69858dc9-0faa-480b-933d-2bff888a117c">IWMPPlugin::GetCaps</a>
 

 

