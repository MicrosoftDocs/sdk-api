---
UID: NF:uiautomationcoreapi.UiaRaiseStructureChangedEvent
title: UiaRaiseStructureChangedEvent function
author: windows-sdk-content
description: Called by a provider to notify the Microsoft UI Automation core that the tree structure has changed.
old-location: winauto\uiauto_UiaRaiseStructureChangedEventFunction.htm
tech.root: WinAuto
ms.assetid: 29137b40-4758-4c73-9596-8cb375b8d362
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: UiaRaiseStructureChangedEvent, UiaRaiseStructureChangedEvent function [Windows Accessibility], uiauto.uiauto_UiaRaiseStructureChangedEventFunction, uiauto_UiaRaiseStructureChangedEventFunction, uiautomationcoreapi/UiaRaiseStructureChangedEvent, winauto.uiauto_UiaRaiseStructureChangedEventFunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaRaiseStructureChangedEvent function


## -description


Called by a provider to notify the Microsoft UI Automation core that the tree structure has changed.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider node where the tree change occurred.


### -param structureChangeType [in]

Type: <b><a href="https://msdn.microsoft.com/abaf9551-40c4-4ab6-adb7-b619f3bc9745">StructureChangeType</a></b>

The type of change that occurred in the tree.


### -param pRuntimeId [in]

Type: <b>int*</b>

The runtime IDs for the child elements of the provider node 
    where the tree change occurred. This parameter is used only when <i>structureChangeType</i> is <a href="uiauto_StructureChangeTypeEnum.htm">StructureChangeType_ChildRemoved</a>; it is <b>NULL</b> for all other structure-change events.

<div class="alert"><b>Note</b>  For Windows 7, the array of integers pointed to by <i>pRuntimeId</i> can contain a partial set of 
    IDs that identify only those elements affected by the structure change.</div>
<div> </div>

### -param cRuntimeIdLen [in]

Type: <b>int</b>

Length of the array of integers.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An example of a change in the tree structure is child elements being added to or removed from a list box, 
                or being expanded or collapsed in a tree view.



