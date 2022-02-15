---
UID: NE:uiautomationcoreapi.TreeScope
title: TreeScope (uiautomationcoreapi.h)
description: Contains values that specify the scope of various operations in the Microsoft UI Automation tree.
helpviewer_keywords: ["TreeScope","TreeScope enumeration [Windows Accessibility]","TreeScope_Ancestors","TreeScope_Children","TreeScope_Descendants","TreeScope_Element","TreeScope_None","TreeScope_Parent","TreeScope_Subtree","uiauto.uiauto_TreeScopeEnum","uiauto_TreeScopeEnum","uiautomationclient/TreeScope","uiautomationclient/TreeScope_Ancestors","uiautomationclient/TreeScope_Children","uiautomationclient/TreeScope_Descendants","uiautomationclient/TreeScope_Element","uiautomationclient/TreeScope_None","uiautomationclient/TreeScope_Parent","uiautomationclient/TreeScope_Subtree","winauto.uiauto_TreeScopeEnum"]
old-location: winauto\uiauto_TreeScopeEnum.htm
tech.root: WinAuto
ms.assetid: eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e
ms.date: 12/05/2018
ms.keywords: TreeScope, TreeScope enumeration [Windows Accessibility], TreeScope_Ancestors, TreeScope_Children, TreeScope_Descendants, TreeScope_Element, TreeScope_None, TreeScope_Parent, TreeScope_Subtree, uiauto.uiauto_TreeScopeEnum, uiauto_TreeScopeEnum, uiautomationclient/TreeScope, uiautomationclient/TreeScope_Ancestors, uiautomationclient/TreeScope_Children, uiautomationclient/TreeScope_Descendants, uiautomationclient/TreeScope_Element, uiautomationclient/TreeScope_None, uiautomationclient/TreeScope_Parent, uiautomationclient/TreeScope_Subtree, winauto.uiauto_TreeScopeEnum
req.header: uiautomationcoreapi.h
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
 - TreeScope
 - uiautomationcoreapi/TreeScope
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
 - TreeScope
---

# TreeScope enumeration


## -description

Contains values that specify the scope of various operations in the Microsoft UI Automation tree.

## -enum-fields

### -field TreeScope_None:0x0

The scope excludes the subtree from the search.

### -field TreeScope_Element:0x1

The scope includes the element itself.

### -field TreeScope_Children:0x2

The scope includes children of the element.

### -field TreeScope_Descendants:0x4

The scope includes children and more distant descendants of the element.

### -field TreeScope_Parent:0x8

The scope includes the parent of the element.

### -field TreeScope_Ancestors:0x10

The scope includes the parent and more distant ancestors of the element.

### -field TreeScope_Subtree

The scope includes the element and all its descendants. This flag is a combination of the TreeScope_Element and TreeScope_Descendants values.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addautomationeventhandler">AddAutomationEventHandler</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler">AddPropertyChangedEventHandler</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray">AddPropertyChangedEventHandlerNativeArray</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler">AddStructureChangedEventHandler</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<b>Reference</b>
