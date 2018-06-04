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

# _WMPortNumberRange structure


## -description



The <b>WM_PORT_NUMBER_RANGE</b> structure describes the range of port numbers used by the <b>IWMReaderNetworkConfig</b> interface.




## -struct-fields




### -field wPortBegin

<b>WORD</b> containing the lowest port number.


### -field wPortEnd

<b>WORD</b> containing the highest port number.


## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/a1792fd0-e9c3-4e28-9928-a615e1c9aec8">IWMReaderNetworkConfig::GetUDPPortRanges</a>



<a href="https://msdn.microsoft.com/9a61943a-8ff9-4504-b76f-25e3c5c8d4a4">IWMReaderNetworkConfig::SetUDPPortRanges</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

