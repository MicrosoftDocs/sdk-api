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

# _PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration


## -description


The <b>PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS</b> enumeration defines the possible client information values.


## -enum-fields




### -field PeerDistClientBasicInfo

 Indicates the information to retrieve is a <a href="https://msdn.microsoft.com/abd98a28-b208-4f31-a28b-ff6ff6677af9">PEERDIST_CLIENT_BASIC_INFO</a> structure.


### -field MaximumPeerDistClientInfoByHandlesClass

The maximum value for the enumeration that is used for error checking.  This value should not be sent to the <a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationByHandle</a> function.


## -remarks



A value from this enumeration is passed to the<a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationByHandle</a> function as the <i>PeerDistClientInfoClass</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationByHandle</a>
 

 

