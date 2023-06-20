---
UID: NF:wmpplug.IWMPPluginUI.TranslateAccelerator
title: IWMPPluginUI::TranslateAccelerator (wmpplug.h)
description: The TranslateAccelerator method is called as part of the Windows Media Player message loop to allow the plug-in to intercept and respond to keyboard events.
helpviewer_keywords: ["IWMPPluginUI interface [Windows Media Player]","TranslateAccelerator method","IWMPPluginUI.TranslateAccelerator","IWMPPluginUI::TranslateAccelerator","IWMPPluginUITranslateAccelerator","TranslateAccelerator","TranslateAccelerator method [Windows Media Player]","TranslateAccelerator method [Windows Media Player]","IWMPPluginUI interface","wmp.iwmppluginui_translateaccelerator","wmpplug/IWMPPluginUI::TranslateAccelerator"]
old-location: wmp\iwmppluginui_translateaccelerator.htm
tech.root: WMP
ms.assetid: 0accc3d7-a194-4f89-a90c-ee3ce10d0e27
ms.date: 4/26/2023
ms.keywords: IWMPPluginUI interface [Windows Media Player],TranslateAccelerator method, IWMPPluginUI.TranslateAccelerator, IWMPPluginUI::TranslateAccelerator, IWMPPluginUITranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [Windows Media Player], TranslateAccelerator method [Windows Media Player],IWMPPluginUI interface, wmp.iwmppluginui_translateaccelerator, wmpplug/IWMPPluginUI::TranslateAccelerator
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
 - IWMPPluginUI::TranslateAccelerator
 - wmpplug/IWMPPluginUI::TranslateAccelerator
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
 - IWMPPluginUI.TranslateAccelerator
---

# IWMPPluginUI::TranslateAccelerator


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>TranslateAccelerator</b> method is called as part of the Windows Media Player message loop to allow the plug-in to intercept and respond to keyboard events.

## -parameters

### -param lpmsg [in]

<b>LPMSG</b> structure containing message information from Windows Media Player that the plug-in can respond to.

## -returns

This method returns an <b>HRESULT</b>.

## -remarks

The plug-in can set up an accelerator table to reroute specific keyboard events to appropriate handler methods. If the plug-in chooses not to respond to keyboard events, it should return <b>S_FALSE</b>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpplug/nn-wmpplug-iwmppluginui">IWMPPluginUI Interface</a>