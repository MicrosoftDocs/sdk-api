---
UID: NE:tabflicks.FLICKMODE
title: FLICKMODE
author: windows-sdk-content
description: Describes where Flick gestures are enabled.
old-location: tablet\flickmode.htm
old-project: tablet
ms.assetid: d8e015dc-033c-47a6-b4fd-6ef3b014e505
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FLICKMODE, FLICKMODE enumeration [Tablet PC], FLICKMODE_OFF, FLICKMODE_ON, d8e015dc-033c-47a6-b4fd-6ef3b014e505, tabflicks/FLICKMODE, tabflicks/FLICKMODE_OFF, tabflicks/FLICKMODE_ON, tablet.flickmode
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
req.typenames: FLICKMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	tabflicks.h
api_name:
-	FLICKMODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# FLICKMODE enumeration


## -description



Describes where Flick gestures are enabled.




## -enum-fields




### -field FLICKMODE_MIN


### -field FLICKMODE_OFF

Pen flicks are not enabled.


### -field FLICKMODE_ON

Pen flicks are enabled.


### -field FLICKMODE_LEARNING


### -field FLICKMODE_MAX


### -field FLICKMODE_DEFAULT




## -remarks



The <b>HKEY_CURRENT_USER\Software\Microsoft\Wisp\Pen\SysEventParameters</b> subkey has an entry called <b>FlickMode</b> that indicates whether pen flicks are enabled. The value of the entry is one of the <b>FLICKMODE</b> enumeration values.




## -see-also




<a href="https://msdn.microsoft.com/004c7d76-90a9-4506-a70b-dbf8f9e1c616">flicks gestures</a>



<a href="https://msdn.microsoft.com/d5c6fa9a-b7a3-4097-bf4f-6d540130f715">responding to pen flicks</a>



<a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">wm_tablet_flick message</a>
 

 

