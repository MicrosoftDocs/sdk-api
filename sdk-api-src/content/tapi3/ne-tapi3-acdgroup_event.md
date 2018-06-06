---
UID: NE:tapi3.ACDGROUP_EVENT
title: ACDGROUP_EVENT
author: windows-sdk-content
description: The ACDGROUP_EVENT enum describes ACD group events. The ITACDGroupEvent::get_Event method returns a member of this enum to indicate the type of ACD group event that occurred.
old-location: tapi3\acdgroup_event.htm
old-project: Tapi
ms.assetid: fb3de7e5-5a29-4f7b-8b2a-252536dedae6
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ACDGE_GROUP_REMOVED, ACDGE_NEW_GROUP, ACDGROUP_EVENT, ACDGROUP_EVENT enumeration [TAPI 2.2], _tapi3_acdgroup_event, tapi3.acdgroup_event, tapi3cc/ACDGE_GROUP_REMOVED, tapi3cc/ACDGE_NEW_GROUP, tapi3cc/ACDGROUP_EVENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: ACDGROUP_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tapi3cc.h
api_name:
 - ACDGROUP_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ACDGROUP_EVENT enumeration


## -description


The 
<b>ACDGROUP_EVENT</b> enum describes ACD group events. The 
<a href="https://msdn.microsoft.com/9bc67911-cfb6-450c-bdc6-ade8d4617271">ITACDGroupEvent::get_Event</a> method returns a member of this enum to indicate the type of ACD group event that occurred.


## -enum-fields




### -field ACDGE_NEW_GROUP

A new ACD group has been added.


### -field ACDGE_GROUP_REMOVED

An ACD group has been removed.


## -see-also




<a href="https://msdn.microsoft.com/9bc67911-cfb6-450c-bdc6-ade8d4617271">ITACDGroupEvent::get_Event</a>
 

 

