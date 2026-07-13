---
UID: NE:uiautomationcore.NavigateDirection
title: NavigateDirection (uiautomationcore.h)
description: Contains values used to specify the direction of navigation within the Microsoft UI Automation tree.
helpviewer_keywords: ["NavigateDirection","NavigateDirection enumeration [Windows Accessibility]","NavigateDirection_FirstChild","NavigateDirection_LastChild","NavigateDirection_NextSibling","NavigateDirection_Parent","NavigateDirection_PreviousSibling","uiauto.uiauto_NavDirEnum","uiauto_NavDirEnum","uiautomationcore/NavigateDirection","uiautomationcore/NavigateDirection_FirstChild","uiautomationcore/NavigateDirection_LastChild","uiautomationcore/NavigateDirection_NextSibling","uiautomationcore/NavigateDirection_Parent","uiautomationcore/NavigateDirection_PreviousSibling","winauto.uiauto_NavDirEnum"]
old-location: winauto\uiauto_NavDirEnum.htm
tech.root: WinAuto
ms.assetid: 33385413-3500-4f80-b53a-fe960d1b53ee
ms.date: 12/05/2018
ms.keywords: NavigateDirection, NavigateDirection enumeration [Windows Accessibility], NavigateDirection_FirstChild, NavigateDirection_LastChild, NavigateDirection_NextSibling, NavigateDirection_Parent, NavigateDirection_PreviousSibling, uiauto.uiauto_NavDirEnum, uiauto_NavDirEnum, uiautomationcore/NavigateDirection, uiautomationcore/NavigateDirection_FirstChild, uiautomationcore/NavigateDirection_LastChild, uiautomationcore/NavigateDirection_NextSibling, uiautomationcore/NavigateDirection_Parent, uiautomationcore/NavigateDirection_PreviousSibling, winauto.uiauto_NavDirEnum
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - NavigateDirection
 - uiautomationcore/NavigateDirection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - NavigateDirection
---

# NavigateDirection enumeration


## -description

Contains values used to specify the direction of navigation within the Microsoft UI Automation tree.

## -enum-fields

### -field NavigateDirection_Parent:0

The navigation direction is to the parent.

### -field NavigateDirection_NextSibling:1

The navigation direction is to the next sibling.

### -field NavigateDirection_PreviousSibling:2

The navigation direction is to the previous sibling.

### -field NavigateDirection_FirstChild:3

The navigation direction is to the first child.

### -field NavigateDirection_LastChild:4

The navigation direction is to the last child.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-navigate">Navigate</a>
