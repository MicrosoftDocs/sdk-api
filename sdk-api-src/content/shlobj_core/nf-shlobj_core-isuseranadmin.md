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

# IsUserAnAdmin function


## -description


<p class="CCE_Message">[<b>IsUserAnAdmin</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Tests whether the current user is a member of the Administrator's group.


## -parameters






## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the user is a member of the Administrator's group; otherwise, <b>FALSE</b>.




## -remarks



This function is a wrapper for <a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a>. It is recommended to call that function directly to determine Administrator group status rather than calling  <b>IsUserAnAdmin</b>.




## -see-also




<a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a>
 

 

