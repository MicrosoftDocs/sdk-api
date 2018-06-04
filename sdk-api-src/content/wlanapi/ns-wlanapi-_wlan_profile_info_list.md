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

# _WLAN_PROFILE_INFO_LIST structure


## -description


The <b>WLAN_PROFILE_INFO_LIST</b> structure contains a list of wireless profile  information.


## -struct-fields




### -field dwNumberOfItems

The number of wireless profile entries in the <b>ProfileInfo</b> member.


### -field dwIndex

The index of the current item.  The index of the first item is 0. The <b>dwIndex</b> member must be less than the <b>dwNumberOfItems</b> member.

This member is not used by the wireless service. Applications can use this member when processing individual profiles in the   <b>WLAN_PROFILE_INFO_LIST</b> structure. When an application passes this structure from one function to another, it can set the value of <b>dwIndex</b> to the index of the item currently being processed. This can help an application maintain state.  

<b>dwIndex</b> should always be initialized before use.


### -field ProfileInfo.unique

 


### -field ProfileInfo.size_is

 


### -field ProfileInfo.size_is.dwNumberOfItems

 


### -field ProfileInfo

An array of <a href="https://msdn.microsoft.com/ca45278c-2e1e-4080-825a-d6a05e463858">WLAN_PROFILE_INFO</a> structures containing interface information. The number of items in the array is specified in the <b>dwNumberOfItems</b> member.


## -see-also




<a href="https://msdn.microsoft.com/ca45278c-2e1e-4080-825a-d6a05e463858">WLAN_PROFILE_INFO</a>



<a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a>



<a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a>
 

 

