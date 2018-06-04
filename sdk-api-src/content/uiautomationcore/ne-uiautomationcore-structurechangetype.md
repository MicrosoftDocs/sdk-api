---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# StructureChangeType enumeration


## -description


Contains values that specify the type of change in the Microsoft UI Automation tree structure.


## -enum-fields




### -field StructureChangeType_ChildAdded

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



