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

# ITunerCap::get_SupportedNetworkTypes


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_SupportedNetworkTypes</b> method retrieves a list of the network types that are supported by the TV tuner.


## -parameters




### -param ulcNetworkTypesMax [in]

The maximum number of network-type GUIDs that the <i>pguidNetworkTypes</i> buffer can hold.


### -param pulcNetworkTypes [out]

Receives a count of the number of network-type GUIDs actually written to the <i>pguidNetworkTypes</i> buffer.


### -param pguidNetworkTypes [in, out]

Receives an array of network-type GUIDs. For the list of valid network-type GUIDs, see <a href="https://msdn.microsoft.com/627e8aaf-7638-4d17-97b5-0aeaad304b98">Default Tuning Spaces</a>.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d7027ff4-4fb9-48c1-b527-92e65009b089">ITunerCap Interface</a>
 

 

