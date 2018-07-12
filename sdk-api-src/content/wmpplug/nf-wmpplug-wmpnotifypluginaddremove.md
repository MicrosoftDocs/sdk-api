---
UID: NF:wmpplug.WMPNotifyPluginAddRemove
title: WMPNotifyPluginAddRemove function
author: windows-sdk-content
description: The WMPNotifyPluginAddRemove function notifies Windows Media Player that a plug-in has been installed or uninstalled.
old-location: wmp\wmpnotifypluginaddremove.htm
old-project: WMP
ms.assetid: e367011a-2151-4324-90da-304dd7f989ab
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: WMPNotifyPluginAddRemove, WMPNotifyPluginAddRemove function [Windows Media Player], wmp.wmpnotifypluginaddremove, wmpplug/WMPNotifyPluginAddRemove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wmpplug.h
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
tech.root: 
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmpplug.h
api_name:
 - WMPNotifyPluginAddRemove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMPNotifyPluginAddRemove function


## -description


The <b>WMPNotifyPluginAddRemove</b> function notifies Windows Media Player that a plug-in has been installed or uninstalled.


## -parameters






## -returns



The return value indicates whether the function call succeeded.




## -remarks



This function is typically called by a user interface (UI) plug-in in its <a href="https://msdn.microsoft.com/4442206b-b2ad-47d7-8add-18002c44c5a2">DllRegisterServer</a> and <a href="https://msdn.microsoft.com/b71137a7-284e-4521-a3b2-9dad9c9d3c54">DllUnregisterServer</a> methods. Windows Media Player Plug-in Wizard generates this code automatically, so it is only necessary to add calls to this function to UI plug-ins created without the wizard.




## -see-also




<a href="https://msdn.microsoft.com/5139412c-bafc-4009-82d2-f9c502118c7d">User Interface Plug-ins Programming Reference</a>
 

 

