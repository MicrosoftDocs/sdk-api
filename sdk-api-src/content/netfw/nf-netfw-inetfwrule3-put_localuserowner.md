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

# INetFwRule3::put_LocalUserOwner


## -description


Specifies the user security identifier (SID) of the user who is the owner of the rule. 

This property is read/write.


## -parameters


## -remarks



If this rule does not specify <b>localUserConditions</b>, all the traffic that this rule matches must be destined to or originated from this user.




## -see-also




<a href="https://msdn.microsoft.com/72bf5ac3-7ee7-4837-96b2-815b499aac2f">INetFwRule3</a>
 

 

