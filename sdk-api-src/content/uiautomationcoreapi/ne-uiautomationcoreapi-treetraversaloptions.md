---
UID: NE:uiautomationcoreapi.TreeTraversalOptions
title: TreeTraversalOptions
author: windows-sdk-content
description: Defines values that can be used to customize tree navigation order.
old-location: winauto\uiauto_TreeTraversalOptions.htm
tech.root: WinAuto
ms.assetid: BB1A65F5-797A-4240-9082-041068A87709
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TreeTraversalOptions, TreeTraversalOptions enumeration [Windows Accessibility], TreeTraversalOptions_Default, TreeTraversalOptions_LastToFirstOrder, TreeTraversalOptions_PostOrder, uiautomationclient/TreeTraversalOptions, uiautomationclient/TreeTraversalOptions_Default, uiautomationclient/TreeTraversalOptions_LastToFirstOrder, uiautomationclient/TreeTraversalOptions_PostOrder, winauto.uiauto_TreeTraversalOptions
ms.topic: enum
req.header: uiautomationcoreapi.h
req.include-header: UIAutomation.h, Uiautomationcoreapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
 - TreeTraversalOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeTraversalOptions enumeration


## -description


Defines values that can be used to customize tree navigation order.


## -enum-fields




### -field TreeTraversalOptions_Default

Pre-order,
    visit children from first to last.



### -field TreeTraversalOptions_PostOrder

Post-order, see Remarks for more info.


### -field TreeTraversalOptions_LastToFirstOrder

Visit children from last to first.


## -remarks



Option groups (flags):

<ul>
<li>Traversal order (pre-order, post-order) defines when nodes should be tested 
against search conditions. For example, "on enter" or "on leave".
</li>
<li> Visit order defines in which order relatives are visited. Relatives include
children and siblings. Visit orders are relative to parents. From the child 
perspective First-to-Last means "visit the next sibling from the child" while
Last-to-First means "visit the previous sibling from the child".
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>
 

 

