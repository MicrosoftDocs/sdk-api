---
UID: NF:wmpplug.IWMPPluginUI.SetCore
title: IWMPPluginUI::SetCore (wmpplug.h)
description: The SetCore method is called by Windows Media Player to provide plug-in access to the core Windows Media Player APIs.
helpviewer_keywords: ["IWMPPluginUI interface [Windows Media Player]","SetCore method","IWMPPluginUI.SetCore","IWMPPluginUI::SetCore","IWMPPluginUISetCore","SetCore","SetCore method [Windows Media Player]","SetCore method [Windows Media Player]","IWMPPluginUI interface","wmp.iwmppluginui_setcore","wmpplug/IWMPPluginUI::SetCore"]
old-location: wmp\iwmppluginui_setcore.htm
tech.root: WMP
ms.assetid: 6b6e6878-1d9d-4f45-94a9-316e86da85df
ms.date: 4/26/2023
ms.keywords: IWMPPluginUI interface [Windows Media Player],SetCore method, IWMPPluginUI.SetCore, IWMPPluginUI::SetCore, IWMPPluginUISetCore, SetCore, SetCore method [Windows Media Player], SetCore method [Windows Media Player],IWMPPluginUI interface, wmp.iwmppluginui_setcore, wmpplug/IWMPPluginUI::SetCore
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
 - IWMPPluginUI::SetCore
 - wmpplug/IWMPPluginUI::SetCore
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
 - IWMPPluginUI.SetCore
---

# IWMPPluginUI::SetCore


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetCore</b> method is called by Windows Media Player to provide plug-in access to the core Windows Media Player APIs.

## -parameters

### -param pCore [in]

Pointer to an <b>IWMPCore</b> interface.

## -returns

This method returns an <b>HRESULT</b>.

## -remarks

This method is called by Windows Media Player to allow the plug-in to set or release a pointer to the <b>IWMPCore</b> interface. If <i>pCore</i> is <b>NULL</b>, the plug-in is being shut down and all stored references to the core should be released.

This method is not called when Windows Media Player instantiates the plug-in for the purpose of displaying its property page. This method can therefore be used as an entry point that will only be called when the plug-in is enabled and Windows Media Player loads it normally.

## -see-also

<a href="/windows/desktop/api/wmpplug/nn-wmpplug-iwmppluginui">IWMPPluginUI Interface</a>