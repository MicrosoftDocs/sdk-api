---
UID: NF:wmpplug.IWMPPluginUI.Create
title: IWMPPluginUI::Create
author: windows-sdk-content
description: The Create method is called by Windows Media Player to instantiate the plug-in user interface. This method is passed a handle to a parent window of the plug-in window. A handle to the newly created window is then passed back to the calling method.
old-location: wmp\iwmppluginui_create.htm
tech.root: WMP
ms.assetid: f7ba2985-42a2-456f-8195-a292c90b440d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: Create, Create method [Windows Media Player], Create method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],Create method, IWMPPluginUI.Create, IWMPPluginUI::Create, IWMPPluginUICreate, wmp.iwmppluginui_create, wmpplug/IWMPPluginUI::Create
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
 - IWMPPluginUI.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmpplug.h
: 
- IWMPPluginUI.Create
: 
---

# IWMPPluginUI::Create


## -description



The <b>Create</b> method is called by Windows Media Player to instantiate the plug-in user interface. This method is passed a handle to a parent window of the plug-in window. A handle to the newly created window is then passed back to the calling method.




## -parameters




### -param hwndParent [in]

<b>HWND</b> handle to a parent window of the plug-in window.


### -param phwndWindow [out]

Pointer to an <b>HWND</b> handle to the plug-in window after the content is filled in.


## -returns



This method returns an <b>HRESULT</b>.




## -remarks



This method is called by Windows Media Player for all user interface plug-in types except the background type.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/f292a3e6-87bf-4e68-8737-f7d6351c4ff4">IWMPPluginUI Interface</a>
 

 

