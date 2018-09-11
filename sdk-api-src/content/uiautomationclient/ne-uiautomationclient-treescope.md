---
UID: NE:uiautomationclient.TreeScope
title: TreeScope
author: windows-sdk-content
description: Contains values that specify the scope of various operations in the Microsoft UI Automation tree.
old-location: winauto\uiauto_TreeScopeEnum.htm
tech.root: WinAuto
ms.assetid: eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TreeScope, TreeScope enumeration [Windows Accessibility], TreeScope_Ancestors, TreeScope_Children, TreeScope_Descendants, TreeScope_Element, TreeScope_None, TreeScope_Parent, TreeScope_Subtree, uiauto.uiauto_TreeScopeEnum, uiauto_TreeScopeEnum, uiautomationclient/TreeScope, uiautomationclient/TreeScope_Ancestors, uiautomationclient/TreeScope_Children, uiautomationclient/TreeScope_Descendants, uiautomationclient/TreeScope_Element, uiautomationclient/TreeScope_None, uiautomationclient/TreeScope_Parent, uiautomationclient/TreeScope_Subtree, winauto.uiauto_TreeScopeEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: uiautomationclient.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationClient.h
api_name:
 - TreeScope
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeScope enumeration


## -description


Contains values that specify the scope of various operations in the Microsoft UI Automation tree.


## -enum-fields




### -field TreeScope_None

The scope excludes the subtree from the search.


### -field TreeScope_Element

The scope includes the element itself.


### -field TreeScope_Children

The scope includes children of the element.


### -field TreeScope_Descendants

The scope includes children and more distant descendants of the element.


### -field TreeScope_Parent

The scope includes the parent of the element.


### -field TreeScope_Ancestors

The scope includes the parent and more distant ancestors of the element.


### -field TreeScope_Subtree

The scope includes the element and all its descendants. This flag is a combination of the TreeScope_Element and TreeScope_Descendants values.


## -see-also




<a href="https://msdn.microsoft.com/15ceca71-33e8-4d66-afd6-3d50fe81c127">AddAutomationEventHandler</a>



<a href="https://msdn.microsoft.com/2623a48e-8818-486c-9bde-b218cde49189">AddPropertyChangedEventHandler</a>



<a href="https://msdn.microsoft.com/0d3cf5c3-5d0e-4214-a9fc-8b0132ad9b77">AddPropertyChangedEventHandlerNativeArray</a>



<a href="https://msdn.microsoft.com/671049a4-50cf-49df-9028-7af38629b7a9">AddStructureChangedEventHandler</a>



<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<b>Reference</b>
 

 

