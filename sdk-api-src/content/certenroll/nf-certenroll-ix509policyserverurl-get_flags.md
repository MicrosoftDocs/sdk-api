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

# IX509PolicyServerUrl::get_Flags


## -description


The <b>Flags</b> property specifies or retrieves a value that indicates whether the certificate enrollment policy (CEP) server policy information can be loaded from group policy, from the registry, or both.

This property is read/write.


## -parameters


## -remarks



When the PsfLocationGroupPolicy and PsfLocationRegistry flags are combined, this method reads policy information from the local registry and combines it with policy information specified by group policy.




## -see-also




<a href="https://msdn.microsoft.com/ad9d61ec-f607-4f71-ad8a-28d821e29c27">IX509PolicyServerUrl</a>
 

 

