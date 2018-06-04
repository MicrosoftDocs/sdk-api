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

# _SIP_CAP_SET_V3 structure


## -description


The <b>SIP_CAP_SET</b> structure defines the capabilities of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP).


## -struct-fields




### -field cbSize

Size, in bytes, of this structure.


### -field dwVersion

The SIP version. By default, this value is two (2).


### -field isMultiSign

A value of one (1) indicates that the SIP supports multiple embedded signatures. Otherwise, set this value to zero (0).


### -field dwFlags

 


### -field dwReserved

Reserved for future use. Set this value to zero (0).

