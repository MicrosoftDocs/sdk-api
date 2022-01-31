---
UID: NE:uiautomationclient.AutomationElementMode
title: AutomationElementMode (uiautomationclient.h)
description: Contains values that specify the type of reference to use when returning UI Automation elements.
helpviewer_keywords: ["AutomationElementMode","AutomationElementMode enumeration [Windows Accessibility]","AutomationElementMode_Full","AutomationElementMode_None","uiauto.uiauto_AutomationElementModeEnum","uiauto_AutomationElementModeEnum","uiautomationclient/AutomationElementMode","uiautomationclient/AutomationElementMode_Full","uiautomationclient/AutomationElementMode_None","winauto.uiauto_AutomationElementModeEnum"]
old-location: winauto\uiauto_AutomationElementModeEnum.htm
tech.root: WinAuto
ms.assetid: b0fadf47-2916-4555-b563-d0b5cd9056e6
ms.date: 12/05/2018
ms.keywords: AutomationElementMode, AutomationElementMode enumeration [Windows Accessibility], AutomationElementMode_Full, AutomationElementMode_None, uiauto.uiauto_AutomationElementModeEnum, uiauto_AutomationElementModeEnum, uiautomationclient/AutomationElementMode, uiautomationclient/AutomationElementMode_Full, uiautomationclient/AutomationElementMode_None, winauto.uiauto_AutomationElementModeEnum
req.header: uiautomationclient.h
req.include-header: UIAutomation.h, Uiautomationcoreapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AutomationElementMode
 - uiautomationclient/AutomationElementMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationClient.h
api_name:
 - AutomationElementMode
---

# AutomationElementMode enumeration


## -description

Contains values that specify the type of reference to use when returning UI Automation elements.

## -enum-fields

### -field AutomationElementMode_None:0

Specifies that returned elements have no reference to the underlying UI and contain only cached information.

### -field AutomationElementMode_Full

Specifies that returned elements have a full reference to the underlying UI.

