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

# MBN_CONTEXT_TYPE enumeration


## -description


The <b>MBN_CONTEXT_TYPE</b> enumerated type specifies the represented context type.


## -enum-fields




### -field MBN_CONTEXT_TYPE_NONE

Context has not yet provisioned for this ID.


### -field MBN_CONTEXT_TYPE_INTERNET

Context represents a connection to the internet.


### -field MBN_CONTEXT_TYPE_VPN

Context represents a connection to a VPN or corporate network.


### -field MBN_CONTEXT_TYPE_VOICE

Context represents a connection to VoIP service.


### -field MBN_CONTEXT_TYPE_VIDEO_SHARE

Context represents a connection to a video share service.


### -field MBN_CONTEXT_TYPE_CUSTOM

Context represents a connection to a custom service.


### -field MBN_CONTEXT_TYPE_PURCHASE

Windows 8 or later: Context represents a purchase connection such as a walled garden, hot-lining, or captive portal.

