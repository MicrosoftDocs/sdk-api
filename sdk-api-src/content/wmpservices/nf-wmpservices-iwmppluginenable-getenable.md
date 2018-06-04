---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
 

 

