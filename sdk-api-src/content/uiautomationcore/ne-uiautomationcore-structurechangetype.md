---
UID: NE:uiautomationcore.StructureChangeType
title: StructureChangeType (uiautomationcore.h)
description: Contains values that specify the type of change in the Microsoft UI Automation tree structure.
helpviewer_keywords: ["StructureChangeType","StructureChangeType enumeration [Windows Accessibility]","StructureChangeType_ChildAdded","StructureChangeType_ChildRemoved","StructureChangeType_ChildrenBulkAdded","StructureChangeType_ChildrenBulkRemoved","StructureChangeType_ChildrenInvalidated","StructureChangeType_ChildrenReordered","uiauto.uiauto_StructureChangeTypeEnum","uiauto_StructureChangeTypeEnum","uiautomationcore/StructureChangeType","uiautomationcore/StructureChangeType_ChildAdded","uiautomationcore/StructureChangeType_ChildRemoved","uiautomationcore/StructureChangeType_ChildrenBulkAdded","uiautomationcore/StructureChangeType_ChildrenBulkRemoved","uiautomationcore/StructureChangeType_ChildrenInvalidated","uiautomationcore/StructureChangeType_ChildrenReordered","winauto.uiauto_StructureChangeTypeEnum"]
old-location: winauto\uiauto_StructureChangeTypeEnum.htm
tech.root: WinAuto
ms.assetid: abaf9551-40c4-4ab6-adb7-b619f3bc9745
ms.date: 12/05/2018
ms.keywords: StructureChangeType, StructureChangeType enumeration [Windows Accessibility], StructureChangeType_ChildAdded, StructureChangeType_ChildRemoved, StructureChangeType_ChildrenBulkAdded, StructureChangeType_ChildrenBulkRemoved, StructureChangeType_ChildrenInvalidated, StructureChangeType_ChildrenReordered, uiauto.uiauto_StructureChangeTypeEnum, uiauto_StructureChangeTypeEnum, uiautomationcore/StructureChangeType, uiautomationcore/StructureChangeType_ChildAdded, uiautomationcore/StructureChangeType_ChildRemoved, uiautomationcore/StructureChangeType_ChildrenBulkAdded, uiautomationcore/StructureChangeType_ChildrenBulkRemoved, uiautomationcore/StructureChangeType_ChildrenInvalidated, uiautomationcore/StructureChangeType_ChildrenReordered, winauto.uiauto_StructureChangeTypeEnum
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
 - StructureChangeType
 - uiautomationcore/StructureChangeType
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
 - StructureChangeType
---

# StructureChangeType enumeration


## -description

Contains values that specify the type of change in the Microsoft UI Automation tree structure.

## -enum-fields

### -field StructureChangeType_ChildAdded:0

A child element was added to the UI Automation element tree.

### -field StructureChangeType_ChildRemoved

A child element was removed from the UI Automation element tree.

### -field StructureChangeType_ChildrenInvalidated

Child elements were invalidated in the UI Automation element tree. This might mean that one or more child elements were added or removed, or a combination of both. This value can also indicate that one subtree in the UI was substituted for another. For example, the entire contents of a dialog box changed at once, or the view of a list changed because an Explorer-type application navigated to another location. The exact meaning depends on the UI Automation provider implementation.

### -field StructureChangeType_ChildrenBulkAdded

Child elements were added in bulk to the UI Automation element tree.

### -field StructureChangeType_ChildrenBulkRemoved

Child elements were removed in bulk from the UI Automation element tree.

### -field StructureChangeType_ChildrenReordered

The order of child elements has changed in the UI Automation element tree. Child elements may or may not have been added or removed.

## -remarks

Because the implementation of structure-change events depends on the underlying UI framework, UI Automation defines no strict rule governing when a provider must switch from sending individual ChildAdded or ChildRemoved events to the bulk equivalent. However, the switch typically occurs when two to five child elements are added or removed at once. The bulk events help to prevent clients from being flooded by individual ChildAdded and ChildRemoved events.

Except for ChildAdded, structure-change events are always associated with the container element that holds the children. The ChildAdded event is associated with the element that was just added.

