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




<a href="https://msdn.microsoft.com/e384aa43-72ab-44b7-b6bd-7a29335b5197">IWMPPlugin Interface</a>



<a href="https://msdn.microsoft.com/0f6cad76-7583-4272-88d7-25a121a0c2b9">WMPPlugin_Caps</a>
 

 

