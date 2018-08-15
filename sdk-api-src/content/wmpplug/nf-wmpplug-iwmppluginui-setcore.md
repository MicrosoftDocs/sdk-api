---
UID: NF:wmpplug.IWMPPluginUI.SetCore
title: IWMPPluginUI::SetCore
author: windows-sdk-content
description: The SetCore method is called by Windows Media Player to provide plug-in access to the core Windows Media Player APIs.
old-location: wmp\iwmppluginui_setcore.htm
old-project: WMP
ms.assetid: 6b6e6878-1d9d-4f45-94a9-316e86da85df
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPluginUI interface [Windows Media Player],SetCore method, IWMPPluginUI.SetCore, IWMPPluginUI::SetCore, IWMPPluginUISetCore, SetCore, SetCore method [Windows Media Player], SetCore method [Windows Media Player],IWMPPluginUI interface, wmp.iwmppluginui_setcore, wmpplug/IWMPPluginUI::SetCore
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
 - IWMPPluginUI.SetCore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPluginUI::SetCore


## -description



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




<a href="https://msdn.microsoft.com/f292a3e6-87bf-4e68-8737-f7d6351c4ff4">IWMPPluginUI Interface</a>
 

 

