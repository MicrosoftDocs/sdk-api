---
UID: NE:wpcevent.tagWPCFLAG_IM_FEATURE
title: WPCFLAG_IM_FEATURE (wpcevent.h)
author: windows-sdk-content
description: Indicates information about the features accessed during an instant messaging interaction.
old-location: parcon\wpcflag_im_feature.htm
tech.root: parcon
ms.assetid: 2e38fb00-21b7-41c7-8fac-09a417408e68
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WPCFLAG_IM_FEATURE, WPCFLAG_IM_FEATURE enumeration, WPCFLAG_IM_FEATURE_ALL, WPCFLAG_IM_FEATURE_AUDIO, WPCFLAG_IM_FEATURE_FILESWAP, WPCFLAG_IM_FEATURE_GAME, WPCFLAG_IM_FEATURE_NONE, WPCFLAG_IM_FEATURE_SENDING, WPCFLAG_IM_FEATURE_SMS, WPCFLAG_IM_FEATURE_URLSWAP, WPCFLAG_IM_FEATURE_VIDEO, parcon.wpcflag_im_feature, wpcevent/WPCFLAG_IM_FEATURE, wpcevent/WPCFLAG_IM_FEATURE_ALL, wpcevent/WPCFLAG_IM_FEATURE_AUDIO, wpcevent/WPCFLAG_IM_FEATURE_FILESWAP, wpcevent/WPCFLAG_IM_FEATURE_GAME, wpcevent/WPCFLAG_IM_FEATURE_NONE, wpcevent/WPCFLAG_IM_FEATURE_SENDING, wpcevent/WPCFLAG_IM_FEATURE_SMS, wpcevent/WPCFLAG_IM_FEATURE_URLSWAP, wpcevent/WPCFLAG_IM_FEATURE_VIDEO
ms.topic: enum
f1_keywords: 
 - "wpcevent/WPCFLAG_IM_FEATURE"
req.header: wpcevent.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wpcevent.h
api_name:
 - WPCFLAG_IM_FEATURE
product: Windows
targetos: Windows
req.typenames: WPCFLAG_IM_FEATURE
req.redist: 
ms.custom: 19H1
---

# WPCFLAG_IM_FEATURE enumeration


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

