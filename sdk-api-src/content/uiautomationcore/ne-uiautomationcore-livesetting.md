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

# LiveSetting enumeration


## -description


Contains possible values for the LiveSetting property. This property is implemented by provider elements that are part of a live region.


## -enum-fields




### -field Off


### -field Polite


### -field Assertive




#### - LiveSetting_Assertive

The provider element sends change notifications when the content of the live region changes, and a client should immediately notify the user of each change.


#### - LiveSetting_Off

The provider element does not send change notifications when the content of the live region changes. A client application will be aware of changes to the live region only if the client handles other events related to the elements in the live region.


#### - LiveSetting_Polite

The provider element sends change notifications when the content of the live region changes, but a client should not interrupt the user to inform the user of changes. Instead, the client should wait until the user is not performing high-priority actions and wants to receive low-priority notifications.


## -see-also




<a href="https://msdn.microsoft.com/5DAE4E4B-A93D-4743-907E-29FC4B6D9101">CachedLiveSetting</a>



<a href="https://msdn.microsoft.com/3510E0AD-FB79-4636-B6EF-AE0FB62AD55C">CurrentLiveSetting</a>
 

 

