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

# _DOT11_NETWORK_LIST structure


## -description


The <b>DOT11_NETWORK_LIST</b> structure contains a list of 802.11 wireless networks.


## -struct-fields




### -field dwNumberOfItems

Contains the number of items in the <b>Network</b> member.


### -field dwIndex

The index of the current item.  The index of the first item is 0. <b>dwIndex</b> must be less than <b>dwNumberOfItems</b>.

This member is not used by the wireless service. Applications can use this member when processing individual networks in the  <b>DOT11_NETWORK_LIST</b>  structure. When an application passes this structure from one function to another, it can set the value of <b>dwIndex</b> to the index of the item currently being processed. This can help an application maintain state.  

<b>dwIndex</b> should always be initialized before use.


### -field Network.unique

 


### -field Network.size_is

 


### -field Network.size_is.dwNumberOfItems

 


### -field Network

An array of <a href="https://msdn.microsoft.com/95f58433-deef-4c47-8f6c-a9e7b0d52dad">DOT11_NETWORK</a> structures that contain 802.11 wireless network information.


## -see-also




<a href="https://msdn.microsoft.com/95f58433-deef-4c47-8f6c-a9e7b0d52dad">DOT11_NETWORK</a>



<a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a>



<a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a>
 

 

