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

# SHRestricted function


## -description


<p class="CCE_Message">[<b>SHRestricted</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a specified administrator policy is in effect. In many cases, applications need to modify certain behaviors to comply with the policies enacted by system administrators.


## -parameters




### -param rest

Type: <b><a href="https://msdn.microsoft.com/14eac1b9-8ef6-4473-81c1-72ba270a9da7">RESTRICTIONS</a></b>

Specifies one of the flags described in the <a href="https://msdn.microsoft.com/14eac1b9-8ef6-4473-81c1-72ba270a9da7">RESTRICTIONS</a> enumerated type.


## -returns



Type: <b>DWORD</b>

Returns nonzero if the specified restriction is in effect, or zero otherwise.



