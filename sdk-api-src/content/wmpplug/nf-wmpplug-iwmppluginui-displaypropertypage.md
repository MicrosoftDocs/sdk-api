---
UID: NF:wmpplug.IWMPPluginUI.DisplayPropertyPage
title: IWMPPluginUI::DisplayPropertyPage (wmpplug.h)
description: The DisplayPropertyPage method is called by Windows Media Player to request that the plug-in display its property page. This method is passed a handle to a parent window of the plug-in property page dialog box.
helpviewer_keywords: ["DisplayPropertyPage","DisplayPropertyPage method [Windows Media Player]","DisplayPropertyPage method [Windows Media Player]","IWMPPluginUI interface","IWMPPluginUI interface [Windows Media Player]","DisplayPropertyPage method","IWMPPluginUI.DisplayPropertyPage","IWMPPluginUI::DisplayPropertyPage","IWMPPluginUIDisplayPropertyPage","wmp.iwmppluginui_displaypropertypage","wmpplug/IWMPPluginUI::DisplayPropertyPage"]
old-location: wmp\iwmppluginui_displaypropertypage.htm
tech.root: WMP
ms.assetid: 29d1438a-164a-460b-9c3e-804417ce362a
ms.date: 4/26/2023
ms.keywords: DisplayPropertyPage, DisplayPropertyPage method [Windows Media Player], DisplayPropertyPage method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],DisplayPropertyPage method, IWMPPluginUI.DisplayPropertyPage, IWMPPluginUI::DisplayPropertyPage, IWMPPluginUIDisplayPropertyPage, wmp.iwmppluginui_displaypropertypage, wmpplug/IWMPPluginUI::DisplayPropertyPage
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
 - IWMPPluginUI::DisplayPropertyPage
 - wmpplug/IWMPPluginUI::DisplayPropertyPage
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
 - IWMPPluginUI.DisplayPropertyPage
---

# IWMPPluginUI::DisplayPropertyPage


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DisplayPropertyPage</b> method is called by Windows Media Player to request that the plug-in display its property page. This method is passed a handle to a parent window of the plug-in property page dialog box.

## -parameters

### -param hwndParent [in]

<b>HWND</b> handle to a parent window of the property page dialog box.

## -returns

This method returns an <b>HRESULT</b>.

## -remarks

This method is called by Windows Media Player only for plug-ins that provide a property page.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpplug/nn-wmpplug-iwmppluginui">IWMPPluginUI Interface</a>