---
UID: NF:wmpplug.IWMPPluginUI.Destroy
title: IWMPPluginUI::Destroy (wmpplug.h)
description: The Destroy method is called by Windows Media Player to shut down the plug-in user interface.helpviewer_keywords: ["Destroy","Destroy method [Windows Media Player]","Destroy method [Windows Media Player]","IWMPPluginUI interface","IWMPPluginUI interface [Windows Media Player]","Destroy method","IWMPPluginUI.Destroy","IWMPPluginUI::Destroy","IWMPPluginUIDestroy","wmp.iwmppluginui_destroy","wmpplug/IWMPPluginUI::Destroy"]
old-location: wmp\iwmppluginui_destroy.htm
tech.root: WMP
ms.assetid: ca78c354-92ae-47d4-82c3-e41eae19f246
ms.date: 12/05/2018
ms.keywords: Destroy, Destroy method [Windows Media Player], Destroy method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],Destroy method, IWMPPluginUI.Destroy, IWMPPluginUI::Destroy, IWMPPluginUIDestroy, wmp.iwmppluginui_destroy, wmpplug/IWMPPluginUI::Destroy
f1_keywords:
- wmpplug/IWMPPluginUI.Destroy
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nn-wmpplug-iwmppluginui">IWMPPluginUI Interface</a>
 

 

