---
UID: NE:tabflicks.KEYMODIFIER
title: KEYMODIFIER
author: windows-sdk-content
description: Determines which, if any, modifier keys were pressed when the flick gesture occurred.
old-location: tablet\keymodifier.htm
tech.root: tablet
ms.assetid: ffb27356-9ad2-4759-bdc4-1025813a7258
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: KEYMODIFIER, KEYMODIFIER enumeration [Tablet PC], KEYMODIFIER_ALTGR, KEYMODIFIER_CONTROL, KEYMODIFIER_EXT, KEYMODIFIER_MENU, KEYMODIFIER_SHIFT, KEYMODIFIER_WIN, ffb27356-9ad2-4759-bdc4-1025813a7258, tabflicks/KEYMODIFIER, tabflicks/KEYMODIFIER_ALTGR, tabflicks/KEYMODIFIER_CONTROL, tabflicks/KEYMODIFIER_EXT, tabflicks/KEYMODIFIER_MENU, tabflicks/KEYMODIFIER_SHIFT, tabflicks/KEYMODIFIER_WIN, tablet.keymodifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tabflicks.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - tabflicks.h
api_name:
 - KEYMODIFIER
product: Windows
targetos: Windows
req.typenames: KEYMODIFIER
req.redist: 
---

# KEYMODIFIER enumeration


## -description



Determines which, if any, modifier keys were pressed when the flick gesture occurred.




## -enum-fields




### -field KEYMODIFIER_CONTROL

The Control key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_MENU

The Menu key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_SHIFT

The Shift key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_WIN

The Windows key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_ALTGR

The Alt key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_EXT

The pressed key's scan code was preceded by a prefix byte that has the value 0xE0 (224).


