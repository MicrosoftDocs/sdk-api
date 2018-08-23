---
UID: NE:tabflicks.FLICKACTION_COMMANDCODE
title: FLICKACTION_COMMANDCODE
author: windows-sdk-content
description: Defines the possible flick actions that can be assigned to a pen flick.
old-location: tablet\flickaction_commandmode.htm
old-project: tablet
ms.assetid: cb923201-5205-494e-bb67-5a908cb570e5
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: FLICKACTION_COMMANDCODE, FLICKACTION_COMMANDCODE enumeration [Tablet PC], FLICKACTION_COMMANDCODE_APPCOMMAND, FLICKACTION_COMMANDCODE_CUSTOMKEY, FLICKACTION_COMMANDCODE_KEYMODIFIER, FLICKACTION_COMMANDCODE_NULL, FLICKACTION_COMMANDCODE_SCROLL, cb923201-5205-494e-bb67-5a908cb570e5, tabflicks/FLICKACTION_COMMANDCODE, tabflicks/FLICKACTION_COMMANDCODE_APPCOMMAND, tabflicks/FLICKACTION_COMMANDCODE_CUSTOMKEY, tabflicks/FLICKACTION_COMMANDCODE_KEYMODIFIER, tabflicks/FLICKACTION_COMMANDCODE_NULL, tabflicks/FLICKACTION_COMMANDCODE_SCROLL, tablet.flickaction_commandmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tabflicks.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FLICKACTION_COMMANDCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tabflicks.h
api_name:
 - FLICKACTION_COMMANDCODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# FLICKACTION_COMMANDCODE enumeration


## -description



Defines the possible flick actions that can be assigned to a pen flick.




## -enum-fields




### -field FLICKACTION_COMMANDCODE_NULL

No action is assigned to the pen flick.


### -field FLICKACTION_COMMANDCODE_SCROLL

A scrolling command is assigned to the pen flick.


### -field FLICKACTION_COMMANDCODE_APPCOMMAND

An application command is assigned to a pen flick.


### -field FLICKACTION_COMMANDCODE_CUSTOMKEY

A customized key sequence is assigned to the pen flick.


### -field FLICKACTION_COMMANDCODE_KEYMODIFIER

A key modifier is assigned to the pen flick.


## -remarks



In Control Panel, the user can assign commands to pen flicks. Four types of actions with pen flicks include:

<ul>
<li>Scroll Up or Scroll Down.</li>
<li>An application command such as Back or Undo</li>
<li>Any keystroke or keystroke combination such as CONTROL+N.</li>
<li>Activating a modifier key such as SHIFT</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f83994ca-7ebe-42bc-bb54-f101a0a62e52">flick_data structure</a>



<a href="https://msdn.microsoft.com/004c7d76-90a9-4506-a70b-dbf8f9e1c616">flicks gestures</a>



<a href="https://msdn.microsoft.com/d5c6fa9a-b7a3-4097-bf4f-6d540130f715">responding to pen flicks</a>



<a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">wm_tablet_flick message</a>
 

 

