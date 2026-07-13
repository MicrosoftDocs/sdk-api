---
UID: NE:wpcevent.tagWPCFLAG_IM_LEAVE_FLAG
title: WPCFLAG_IM_LEAVE (wpcevent.h)
description: Indicates information about when a participant leaves the instant messaging interaction.
helpviewer_keywords: ["WPCFLAG_IM_LEAVE","WPCFLAG_IM_LEAVE enumeration","WPCFLAG_IM_LEAVE_CONVERSATION_END","WPCFLAG_IM_LEAVE_FORCED","WPCFLAG_IM_LEAVE_NORMAL","parcon.wpcflag_im_leave_flag","wpcevent/WPCFLAG_IM_LEAVE","wpcevent/WPCFLAG_IM_LEAVE_CONVERSATION_END","wpcevent/WPCFLAG_IM_LEAVE_FORCED","wpcevent/WPCFLAG_IM_LEAVE_NORMAL"]
old-location: parcon\wpcflag_im_leave_flag.htm
tech.root: parcon
ms.assetid: d1ca0b51-5d58-4df2-877b-73a02fe1c67d
ms.date: 12/05/2018
ms.keywords: WPCFLAG_IM_LEAVE, WPCFLAG_IM_LEAVE enumeration, WPCFLAG_IM_LEAVE_CONVERSATION_END, WPCFLAG_IM_LEAVE_FORCED, WPCFLAG_IM_LEAVE_NORMAL, parcon.wpcflag_im_leave_flag, wpcevent/WPCFLAG_IM_LEAVE, wpcevent/WPCFLAG_IM_LEAVE_CONVERSATION_END, wpcevent/WPCFLAG_IM_LEAVE_FORCED, wpcevent/WPCFLAG_IM_LEAVE_NORMAL
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
targetos: Windows
req.typenames: WPCFLAG_IM_LEAVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWPCFLAG_IM_LEAVE_FLAG
 - wpcevent/tagWPCFLAG_IM_LEAVE_FLAG
 - WPCFLAG_IM_LEAVE
 - wpcevent/WPCFLAG_IM_LEAVE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wpcevent.h
api_name:
 - WPCFLAG_IM_LEAVE
---

# WPCFLAG_IM_LEAVE enumeration


## -description

Indicates information about when a participant leaves the instant messaging  interaction.

## -enum-fields

### -field WPCFLAG_IM_LEAVE_NORMAL:0x00000000

An instant message participant left the interaction.

### -field WPCFLAG_IM_LEAVE_FORCED:0x00000001

An instant message participant was forced to leave the interaction.

### -field WPCFLAG_IM_LEAVE_CONVERSATION_END

This marks the end of the entire conversation.

