---
UID: NF:wmpplug.IWMPPluginUI.Destroy
title: IWMPPluginUI::Destroy (wmpplug.h)
description: The Destroy method is called by Windows Media Player to shut down the plug-in user interface.
helpviewer_keywords: ["Destroy","Destroy method [Windows Media Player]","Destroy method [Windows Media Player]","IWMPPluginUI interface","IWMPPluginUI interface [Windows Media Player]","Destroy method","IWMPPluginUI.Destroy","IWMPPluginUI::Destroy","IWMPPluginUIDestroy","wmp.iwmppluginui_destroy","wmpplug/IWMPPluginUI::Destroy"]
old-location: wmp\iwmppluginui_destroy.htm
tech.root: WMP
ms.assetid: ca78c354-92ae-47d4-82c3-e41eae19f246
ms.date: 4/26/2023
ms.keywords: Destroy, Destroy method [Windows Media Player], Destroy method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],Destroy method, IWMPPluginUI.Destroy, IWMPPluginUI::Destroy, IWMPPluginUIDestroy, wmp.iwmppluginui_destroy, wmpplug/IWMPPluginUI::Destroy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPPluginUI::Destroy
 - wmpplug/IWMPPluginUI::Destroy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpplug.h
api_name:
 - IWMPPluginUI.Destroy
---

# IWMPPluginUI::Destroy


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Destroy</b> method is called by Windows Media Player to shut down the plug-in user interface. This occurs when the user closes a plug-in in a separate window, switches out of the <b>Now Playing</b> pane, or selects a different display, settings, or metadata area plug-in to display in the <b>Now Playing</b> pane.



## -returns

This method returns an <b>HRESULT</b>.

## -remarks

This method is called by Windows Media Player for all user interface plug-in types except the background type.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpplug/nn-wmpplug-iwmppluginui">IWMPPluginUI Interface</a>
