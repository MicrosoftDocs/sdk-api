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
 

 

