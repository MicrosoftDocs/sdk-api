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

# tagEapPeerMethodOuput structure


## -description


Contains the action information returned by an EAP peer method.


## -struct-fields




### -field action


<a href="https://msdn.microsoft.com/def7e04e-ed0c-46f0-97d6-4c0ab021fa8b">EapPeerMethodResponseAction</a> enumeration value that indicates the response EAPHost should take as a result of the EAP peer method operation.


### -field fAllowNotifications

If <b>TRUE</b>, allows EAPHost to raise a notification to the user; otherwise, do not allow notifications.


## -see-also




<a href="https://msdn.microsoft.com/546ef715-8f51-4f5a-a569-8bf64d52de85">EAPHost Peer Method Structures</a>
 

 

