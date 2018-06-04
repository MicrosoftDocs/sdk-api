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

# tagWPCFLAG_IM_FEATURE enumeration


## -description


Indicates information about the features accessed during an instant messaging interaction.


## -enum-fields




### -field WPCFLAG_IM_FEATURE_NONE

No instant messaging features were used.


### -field WPCFLAG_IM_FEATURE_VIDEO

The video feature was used during the instant messaging session.


### -field WPCFLAG_IM_FEATURE_AUDIO

The audio feature was used during the instant messaging session.


### -field WPCFLAG_IM_FEATURE_GAME

The game feature was used during the instant messaging session.


### -field WPCFLAG_IM_FEATURE_SMS

The short message service feature was used during the instant messaging session.


### -field WPCFLAG_IM_FEATURE_FILESWAP

Files were swapped during the instant messaging session.


### -field WPCFLAG_IM_FEATURE_URLSWAP

URL or website locations were swapped during the instant messaging session.


### -field WPCFLAG_IM_FEATURE_SENDING

The top bit means sending or receiving.


### -field WPCFLAG_IM_FEATURE_ALL

All features were used during the instant messaging session

