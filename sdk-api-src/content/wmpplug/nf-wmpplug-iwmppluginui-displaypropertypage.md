---
UID: NF:wmpplug.IWMPPluginUI.DisplayPropertyPage
title: IWMPPluginUI::DisplayPropertyPage (wmpplug.h)
description: The DisplayPropertyPage method is called by Windows Media Player to request that the plug-in display its property page. This method is passed a handle to a parent window of the plug-in property page dialog box.
helpviewer_keywords: ["DisplayPropertyPage","DisplayPropertyPage method [Windows Media Player]","DisplayPropertyPage method [Windows Media Player]","IWMPPluginUI interface","IWMPPluginUI interface [Windows Media Player]","DisplayPropertyPage method","IWMPPluginUI.DisplayPropertyPage","IWMPPluginUI::DisplayPropertyPage","IWMPPluginUIDisplayPropertyPage","wmp.iwmppluginui_displaypropertypage","wmpplug/IWMPPluginUI::DisplayPropertyPage"]
old-location: wmp\iwmppluginui_displaypropertypage.htm
tech.root: WMP
ms.assetid: 29d1438a-164a-460b-9c3e-804417ce362a
ms.date: 12/05/2018
ms.keywords: DisplayPropertyPage, DisplayPropertyPage method [Windows Media Player], DisplayPropertyPage method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],DisplayPropertyPage method, IWMPPluginUI.DisplayPropertyPage, IWMPPluginUI::DisplayPropertyPage, IWMPPluginUIDisplayPropertyPage, wmp.iwmppluginui_displaypropertypage, wmpplug/IWMPPluginUI::DisplayPropertyPage
f1_keywords:
- wmpplug/IWMPPluginUI.DisplayPropertyPage
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
- IWMPPluginUI.DisplayPropertyPage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPluginUI::DisplayPropertyPage


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nn-wmpplug-iwmppluginui">IWMPPluginUI Interface</a>
 

 

