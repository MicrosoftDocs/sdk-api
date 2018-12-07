---
UID: NF:wmpservices.IWMPPluginEnable.GetEnable
title: IWMPPluginEnable::GetEnable
author: windows-sdk-content
description: The IWMPPluginEnable::GetEnable method returns a value indicating whether Windows Media Player has enabled the plug-in.
old-location: wmp\iwmppluginenable_getenable.htm
tech.root: WMP
ms.assetid: 29a08f6e-17a7-4bff-9aea-d5586d2b55b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnable, GetEnable method [Windows Media Player], GetEnable method [Windows Media Player],IWMPPluginEnable interface, IWMPPluginEnable interface [Windows Media Player],GetEnable method, IWMPPluginEnable.GetEnable, IWMPPluginEnable::GetEnable, IWMPPluginEnableGetEnableDSP, wmp.iwmppluginenable_getenable, wmpservices/IWMPPluginEnable::GetEnable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmpservices.h
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
 - wmpservices.h
api_name:
 - IWMPPluginEnable.GetEnable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPluginEnable::GetEnable


## -description



The <b>IWMPPluginEnable::GetEnable</b> method returns a value indicating whether Windows Media Player has enabled the plug-in.




## -parameters




### -param pfEnable [out]

Pointer to a <b>Boolean</b> value indicating whether the user has enabled the plug-in.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



This value is set by Windows Media Player in the <b>IWMPPluginEnable::SetEnable</b> method.




## -see-also




<a href="https://msdn.microsoft.com/997708e2-18fa-436f-9ca1-cdde5c7414fc">IWMPPluginEnable Interface</a>



<a href="https://msdn.microsoft.com/a0b8e79b-e9bd-40e5-ab58-11469406110a">IWMPPluginEnable::SetEnable</a>
 

 

