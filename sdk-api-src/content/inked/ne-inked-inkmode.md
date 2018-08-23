---
UID: NE:inked.InkMode
title: InkMode
author: windows-sdk-content
description: Specifies the collection mode for drawn ink-whether ink collection is disabled, ink is collected, or ink and gestures are collected.
old-location: tablet\inkmode.htm
old-project: tablet
ms.assetid: 81aac302-c89a-42ca-9c90-170611a8995a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 81aac302-c89a-42ca-9c90-170611a8995a, IM_Disabled, IM_Ink, IM_InkAndGesture, InkMode, InkMode enumeration [Tablet PC], inked/IM_Disabled, inked/IM_Ink, inked/IM_InkAndGesture, inked/InkMode, tablet.inkmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: inked.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
tech.root: 
req.typenames: InkMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - InkMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# InkMode enumeration


## -description



Specifies the collection mode for drawn ink-whether ink collection is disabled, ink is collected, or ink and gestures are collected.




## -enum-fields




### -field IEM_Disabled


### -field IEM_Ink


### -field IEM_InkAndGesture




#### - IM_Disabled

Ink collection is disabled. No strokes are created when in this mode.


#### - IM_Ink

Ink only is collected, creating a stroke.


#### - IM_InkAndGesture

Default. Ink is collected and single-stroke gestures are accepted.


## -see-also




<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit Control Reference</a>



<a href="https://msdn.microsoft.com/26023012-9ab1-4bd9-beff-41587bc74f5e">InkEdit Messages</a>



<a href="https://msdn.microsoft.com/0e395907-108b-40cf-819b-65a34e4ffc4d">InkEdit::InkMode Property</a>
 

 

