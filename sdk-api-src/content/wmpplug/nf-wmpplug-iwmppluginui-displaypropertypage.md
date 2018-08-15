---
UID: NF:wmpplug.IWMPPluginUI.DisplayPropertyPage
title: IWMPPluginUI::DisplayPropertyPage
author: windows-sdk-content
description: The DisplayPropertyPage method is called by Windows Media Player to request that the plug-in display its property page. This method is passed a handle to a parent window of the plug-in property page dialog box.
old-location: wmp\iwmppluginui_displaypropertypage.htm
old-project: WMP
ms.assetid: 29d1438a-164a-460b-9c3e-804417ce362a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DisplayPropertyPage, DisplayPropertyPage method [Windows Media Player], DisplayPropertyPage method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],DisplayPropertyPage method, IWMPPluginUI.DisplayPropertyPage, IWMPPluginUI::DisplayPropertyPage, IWMPPluginUIDisplayPropertyPage, wmp.iwmppluginui_displaypropertypage, wmpplug/IWMPPluginUI::DisplayPropertyPage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmpplug.h
req.include-header: 
req.redist: 
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
 - COM
api_location:
 - wmpplug.h
api_name:
 - IWMPPluginUI.DisplayPropertyPage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/f292a3e6-87bf-4e68-8737-f7d6351c4ff4">IWMPPluginUI Interface</a>
 

 

