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

# drt_status_tag enumeration


## -description


The <b>DRT_STATUS</b> enumeration defines the status of a local DRT instance.


## -enum-fields




### -field DRT_ACTIVE

The local node is connected to the DRT mesh and participating in the DRT system. This is also an indication that remote nodes exist and are present in the cache of the local node.


### -field DRT_ALONE

The local node is participating in the DRT system, but is waiting for remote nodes to join the DRT mesh. This is an indication that remote nodes do not exist, or are not yet present in the cache of the local node.


### -field DRT_NO_NETWORK

The local node does not have network connectivity.


### -field DRT_FAULTED

A critical error has occurred in the local DRT instance. The <a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a> function must be called, after which  an attempt to re-open the DRT can be made. 


## -see-also




<a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>
 

 

