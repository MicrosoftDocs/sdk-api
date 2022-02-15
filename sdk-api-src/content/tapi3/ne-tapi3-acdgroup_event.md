---
UID: NE:tapi3.ACDGROUP_EVENT
title: ACDGROUP_EVENT (tapi3.h)
description: The ACDGROUP_EVENT enum describes ACD group events. The ITACDGroupEvent::get_Event method returns a member of this enum to indicate the type of ACD group event that occurred.
helpviewer_keywords: ["ACDGE_GROUP_REMOVED","ACDGE_NEW_GROUP","ACDGROUP_EVENT","ACDGROUP_EVENT enumeration [TAPI 2.2]","_tapi3_acdgroup_event","tapi3.acdgroup_event","tapi3cc/ACDGE_GROUP_REMOVED","tapi3cc/ACDGE_NEW_GROUP","tapi3cc/ACDGROUP_EVENT"]
old-location: tapi3\acdgroup_event.htm
tech.root: tapi3
ms.assetid: fb3de7e5-5a29-4f7b-8b2a-252536dedae6
ms.date: 12/05/2018
ms.keywords: ACDGE_GROUP_REMOVED, ACDGE_NEW_GROUP, ACDGROUP_EVENT, ACDGROUP_EVENT enumeration [TAPI 2.2], _tapi3_acdgroup_event, tapi3.acdgroup_event, tapi3cc/ACDGE_GROUP_REMOVED, tapi3cc/ACDGE_NEW_GROUP, tapi3cc/ACDGROUP_EVENT
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACDGROUP_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ACDGROUP_EVENT
 - tapi3/ACDGROUP_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tapi3cc.h
api_name:
 - ACDGROUP_EVENT
---

# ACDGROUP_EVENT enumeration


## -description

The 
<b>ACDGROUP_EVENT</b> enum describes ACD group events. The 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itacdgroupevent-get_event">ITACDGroupEvent::get_Event</a> method returns a member of this enum to indicate the type of ACD group event that occurred.

## -enum-fields

### -field ACDGE_NEW_GROUP:0

A new ACD group has been added.

### -field ACDGE_GROUP_REMOVED

An ACD group has been removed.

## -see-also

<a href="/windows/desktop/api/tapi3/nf-tapi3-itacdgroupevent-get_event">ITACDGroupEvent::get_Event</a>
