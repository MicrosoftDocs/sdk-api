---
UID: NE:uiautomationcore.ExpandCollapseState
title: ExpandCollapseState (uiautomationcore.h)
description: Contains values that specify the state of a UI element that can be expanded and collapsed.
helpviewer_keywords: ["ExpandCollapseState","ExpandCollapseState enumeration [Windows Accessibility]","ExpandCollapseState_Collapsed","ExpandCollapseState_Expanded","ExpandCollapseState_LeafNode","ExpandCollapseState_PartiallyExpanded","uiauto.uiauto_ExpandCollapseStateEnum","uiauto_ExpandCollapseStateEnum","uiautomationcore/ExpandCollapseState","uiautomationcore/ExpandCollapseState_Collapsed","uiautomationcore/ExpandCollapseState_Expanded","uiautomationcore/ExpandCollapseState_LeafNode","uiautomationcore/ExpandCollapseState_PartiallyExpanded","winauto.uiauto_ExpandCollapseStateEnum"]
old-location: winauto\uiauto_ExpandCollapseStateEnum.htm
tech.root: WinAuto
ms.assetid: 9625a50d-b9fb-4f85-8245-c77cc53445c3
ms.date: 12/05/2018
ms.keywords: ExpandCollapseState, ExpandCollapseState enumeration [Windows Accessibility], ExpandCollapseState_Collapsed, ExpandCollapseState_Expanded, ExpandCollapseState_LeafNode, ExpandCollapseState_PartiallyExpanded, uiauto.uiauto_ExpandCollapseStateEnum, uiauto_ExpandCollapseStateEnum, uiautomationcore/ExpandCollapseState, uiautomationcore/ExpandCollapseState_Collapsed, uiautomationcore/ExpandCollapseState_Expanded, uiautomationcore/ExpandCollapseState_LeafNode, uiautomationcore/ExpandCollapseState_PartiallyExpanded, winauto.uiauto_ExpandCollapseStateEnum
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
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
 - ExpandCollapseState
 - uiautomationcore/ExpandCollapseState
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
 - ExpandCollapseState
---

# ExpandCollapseState enumeration


## -description

Contains values that specify the state of a UI element that can be expanded and collapsed.

## -enum-fields

### -field ExpandCollapseState_Collapsed:0

No children are visible.

### -field ExpandCollapseState_Expanded:1

All children are visible.

### -field ExpandCollapseState_PartiallyExpanded:2

Some, but not all, children are visible.

### -field ExpandCollapseState_LeafNode:3

The element does not expand or collapse.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iexpandcollapseprovider">IExpandCollapseProvider</a>
