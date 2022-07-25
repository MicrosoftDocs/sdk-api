---
UID: NE:uiautomationclient.PropertyConditionFlags
title: PropertyConditionFlags (uiautomationclient.h)
description: Contains values used in creating property conditions.
helpviewer_keywords: ["PropertyConditionFlags","PropertyConditionFlags enumeration [Windows Accessibility]","PropertyConditionFlags_IgnoreCase","PropertyConditionFlags_MatchSubstring","PropertyConditionFlags_None","uiauto.uiauto_PropertyConditionFlagsEnum","uiauto_PropertyConditionFlagsEnum","uiautomationclient/PropertyConditionFlags","uiautomationclient/PropertyConditionFlags_IgnoreCase","uiautomationclient/PropertyConditionFlags_MatchSubstring","uiautomationclient/PropertyConditionFlags_None","winauto.uiauto_PropertyConditionFlagsEnum"]
old-location: winauto\uiauto_PropertyConditionFlagsEnum.htm
tech.root: WinAuto
ms.assetid: debe8141-2a91-4774-b533-d6f3ccfc7744
ms.date: 12/05/2018
ms.keywords: PropertyConditionFlags, PropertyConditionFlags enumeration [Windows Accessibility], PropertyConditionFlags_IgnoreCase, PropertyConditionFlags_MatchSubstring, PropertyConditionFlags_None, uiauto.uiauto_PropertyConditionFlagsEnum, uiauto_PropertyConditionFlagsEnum, uiautomationclient/PropertyConditionFlags, uiautomationclient/PropertyConditionFlags_IgnoreCase, uiautomationclient/PropertyConditionFlags_MatchSubstring, uiautomationclient/PropertyConditionFlags_None, winauto.uiauto_PropertyConditionFlagsEnum
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
 - PropertyConditionFlags
 - uiautomationclient/PropertyConditionFlags
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
 - PropertyConditionFlags
---

# PropertyConditionFlags enumeration


## -description

Contains values used in creating property conditions.

## -enum-fields

### -field PropertyConditionFlags_None:0

No flags.

### -field PropertyConditionFlags_IgnoreCase:0x1

Comparison of string properties is not case-sensitive.

### -field PropertyConditionFlags_MatchSubstring:0x2

[Windows 10 October 2018 Update (version 1809) and newer]

Comparison of substring properties is enabled.

