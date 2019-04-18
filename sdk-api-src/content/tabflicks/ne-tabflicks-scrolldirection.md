---
UID: NE:tabflicks.SCROLLDIRECTION
title: SCROLLDIRECTION (tabflicks.h)
author: windows-sdk-content
description: Defines the direction of the scrolling command for a pen flick.
old-location: tablet\scrolldirection.htm
tech.root: tablet
ms.assetid: 79d64632-a0ac-4c1b-83e3-76c9fbd11da9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 79d64632-a0ac-4c1b-83e3-76c9fbd11da9, SCROLLDIRECTION, SCROLLDIRECTION enumeration [Tablet PC], SCROLLDIRECTION_DOWN, SCROLLDIRECTION_UP, tabflicks/SCROLLDIRECTION, tabflicks/SCROLLDIRECTION_DOWN, tabflicks/SCROLLDIRECTION_UP, tablet.scrolldirection
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
 - SCROLLDIRECTION
product: Windows
targetos: Windows
req.typenames: SCROLLDIRECTION
req.redist: 
ms.custom: 19H1
---

# SCROLLDIRECTION enumeration


## -description



Defines the direction of the scrolling command for a pen flick.




## -enum-fields




### -field SCROLLDIRECTION_UP

 The flick action is a Scroll Up command.


### -field SCROLLDIRECTION_DOWN

The flick action is a Scroll Down command.


## -remarks



When the user performs a pen flick that is assigned to a scrolling command, the <a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">WM_TABLET_FLICK Message</a> sends the direction of the scrolling command as part of the <a href="https://msdn.microsoft.com/f83994ca-7ebe-42bc-bb54-f101a0a62e52">FLICK_DATA Structure</a>.




## -see-also




<a href="https://msdn.microsoft.com/f83994ca-7ebe-42bc-bb54-f101a0a62e52">flick_data structure</a>



<a href="https://msdn.microsoft.com/004c7d76-90a9-4506-a70b-dbf8f9e1c616">flicks gestures</a>



<a href="https://msdn.microsoft.com/d5c6fa9a-b7a3-4097-bf4f-6d540130f715">responding to pen flicks</a>



<a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">wm_tablet_flick message</a>
 

 

