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

# _WCM_PROFILE_INFO structure


## -description


The <b>WCM_PROFILE_INFO</b> structure contains information about a specific profile.


## -struct-fields




### -field strProfileName

Type: <b>WCHAR[WCM_MAX_PROFILE_NAME]</b>

The profile name.


### -field AdapterGUID

Type: <b>GUID</b>

The GUID of the adapter.


### -field Media

Type: <b><a href="https://msdn.microsoft.com/76617f35-c7a1-49ff-a630-482f2fe45dd7">WCM_MEDIA_TYPE</a></b>

The media type for the profile.


## -see-also




<a href="https://msdn.microsoft.com/76617f35-c7a1-49ff-a630-482f2fe45dd7">WCM_MEDIA_TYPE</a>
 

 

