---
UID: NF:uiautomationcoreapi.UiaRaiseStructureChangedEvent
title: UiaRaiseStructureChangedEvent function (uiautomationcoreapi.h)
description: Called by a provider to notify the Microsoft UI Automation core that the tree structure has changed.
helpviewer_keywords: ["UiaRaiseStructureChangedEvent","UiaRaiseStructureChangedEvent function [Windows Accessibility]","uiauto.uiauto_UiaRaiseStructureChangedEventFunction","uiauto_UiaRaiseStructureChangedEventFunction","uiautomationcoreapi/UiaRaiseStructureChangedEvent","winauto.uiauto_UiaRaiseStructureChangedEventFunction"]
old-location: winauto\uiauto_UiaRaiseStructureChangedEventFunction.htm
tech.root: WinAuto
ms.assetid: 29137b40-4758-4c73-9596-8cb375b8d362
ms.date: 09/24/2020
ms.keywords: UiaRaiseStructureChangedEvent, UiaRaiseStructureChangedEvent function [Windows Accessibility], uiauto.uiauto_UiaRaiseStructureChangedEventFunction, uiauto_UiaRaiseStructureChangedEventFunction, uiautomationcoreapi/UiaRaiseStructureChangedEvent, winauto.uiauto_UiaRaiseStructureChangedEventFunction
req.header: uiautomationcoreapi.h
req.include-header: 
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaRaiseStructureChangedEvent
 - uiautomationcoreapi/UiaRaiseStructureChangedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-uiacore-l1-1-0.dll
 - Ext-MS-Win-UIaCore-l1-1-1.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseStructureChangedEvent
---

# UiaRaiseStructureChangedEvent function

## -description

Called by a provider to notify the Microsoft UI Automation core that the tree structure has changed.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider node where the tree change occurred.

### -param structureChangeType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-structurechangetype">StructureChangeType</a></b>

The type of change that occurred in the tree.

### -param pRuntimeId [in]

Type: <b>int*</b>

The runtime IDs for the child elements of the provider node where the tree change occurred. This parameter is used only when <i>structureChangeType</i> is <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-structurechangetype">StructureChangeType_ChildRemoved</a>; it is <b>NULL</b> for all other structure-change events.

<div class="alert"><b>Note</b>  For Windows 7, the array of integers pointed to by <i>pRuntimeId</i> can contain a partial set of IDs that identify only those elements affected by the structure change.</div>

### -param cRuntimeIdLen [in]

Type: <b>int</b>

Length of the array of integers.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An example of a change in the tree structure is child elements being added to or removed from a list box, or being expanded or collapsed in a tree view.
