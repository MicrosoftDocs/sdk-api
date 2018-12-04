---
UID: NF:wmpplug.IWMPPluginUI.Destroy
title: IWMPPluginUI::Destroy
author: windows-sdk-content
description: The Destroy method is called by Windows Media Player to shut down the plug-in user interface.
old-location: wmp\iwmppluginui_destroy.htm
tech.root: WMP
ms.assetid: ca78c354-92ae-47d4-82c3-e41eae19f246
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Destroy, Destroy method [Windows Media Player], Destroy method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],Destroy method, IWMPPluginUI.Destroy, IWMPPluginUI::Destroy, IWMPPluginUIDestroy, wmp.iwmppluginui_destroy, wmpplug/IWMPPluginUI::Destroy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpplug.h
api_name:
 - IWMPPluginUI.Destroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPluginUI::Destroy


## -description



The <b>Destroy</b> method is called by Windows Media Player to shut down the plug-in user interface. This occurs when the user closes a plug-in in a separate window, switches out of the <b>Now Playing</b> pane, or selects a different display, settings, or metadata area plug-in to display in the <b>Now Playing</b> pane.




## -parameters






## -returns



This method returns an <b>HRESULT</b>.




## -remarks



This method is called by Windows Media Player for all user interface plug-in types except the background type.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/f292a3e6-87bf-4e68-8737-f7d6351c4ff4">IWMPPluginUI Interface</a>
 

 

