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

# DWMNCRENDERINGPOLICY enumeration


## -description


Flags used by the <a href="https://msdn.microsoft.com/51f6544a-edc4-4d0c-b39a-277a8dcbe94f">DwmSetWindowAttribute</a> function to specify the non-client area rendering policy.


## -enum-fields




### -field DWMNCRP_USEWINDOWSTYLE

The non-client rendering area is rendered based on the window style.


### -field DWMNCRP_DISABLED

The non-client area rendering is disabled; the window style is ignored.


### -field DWMNCRP_ENABLED

The non-client area rendering is enabled; the window style is ignored.


### -field DWMNCRP_LAST

The maximum recognized <a href="https://msdn.microsoft.com/b02f9157-55cc-4965-9836-2b359f3dade5">DWMNCRENDERINGPOLICY</a> value, used for validation purposes.


## -remarks



To use a <b>DWMNCRENDERINGPOLICY</b> value, set the <i>dwAttribute</i> parameter of the <a href="https://msdn.microsoft.com/51f6544a-edc4-4d0c-b39a-277a8dcbe94f">DwmSetWindowAttribute</a> function to <b>DWMWA_NCRENDERING_POLICY</b>. Set the <i>pvAttribute</i> parameter to the <b>DWMNCRENDERINGPOLICY</b> value.



