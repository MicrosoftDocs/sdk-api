---
UID: NE:tabflicks.FLICKMODE
title: FLICKMODE (tabflicks.h)
description: Describes where Flick gestures are enabled.
helpviewer_keywords: ["FLICKMODE","FLICKMODE enumeration [Tablet PC]","FLICKMODE_OFF","FLICKMODE_ON","d8e015dc-033c-47a6-b4fd-6ef3b014e505","tabflicks/FLICKMODE","tabflicks/FLICKMODE_OFF","tabflicks/FLICKMODE_ON","tablet.flickmode"]
old-location: tablet\flickmode.htm
tech.root: tablet
ms.assetid: d8e015dc-033c-47a6-b4fd-6ef3b014e505
ms.date: 12/05/2018
ms.keywords: FLICKMODE, FLICKMODE enumeration [Tablet PC], FLICKMODE_OFF, FLICKMODE_ON, d8e015dc-033c-47a6-b4fd-6ef3b014e505, tabflicks/FLICKMODE, tabflicks/FLICKMODE_OFF, tabflicks/FLICKMODE_ON, tablet.flickmode
f1_keywords:
- tabflicks/FLICKMODE
dev_langs:
- c++
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
- FLICKMODE
targetos: Windows
req.typenames: FLICKMODE
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/tablet/flicks-gestures">flicks gestures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ms703447(v=vs.85)">responding to pen flicks</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/wm-tablet-flick-message">wm_tablet_flick message</a>
 

 

