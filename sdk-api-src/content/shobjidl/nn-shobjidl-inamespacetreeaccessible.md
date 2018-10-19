---
UID: NN:shobjidl.INameSpaceTreeAccessible
title: INameSpaceTreeAccessible
author: windows-sdk-content
description: Exposes methods that perform accessibility actions on a Shell item from a namespace tree control.
old-location: shell\INameSpaceTreeAccessible.htm
tech.root: shell
ms.assetid: b14dfe40-e21a-4208-835f-e0febef60783
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: INameSpaceTreeAccessible, INameSpaceTreeAccessible interface [Windows Shell], INameSpaceTreeAccessible interface [Windows Shell],described, _shell_INameSpaceTreeAccessible, shell.INameSpaceTreeAccessible, shobjidl/INameSpaceTreeAccessible
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeAccessible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeAccessible interface


## -description


Exposes methods that perform accessibility actions on a Shell item from a namespace tree control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeAccessible</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INameSpaceTreeAccessible</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INameSpaceTreeAccessible</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6aa6588-6e3c-4229-8540-0aa5d85c0381">OnDoDefaultAccessibilityAction</a>
</td>
<td align="left" width="63%">
Invokes the default accessibility action on a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9de27a09-dc11-46a6-a233-696ccf35aa87">OnGetAccessibilityRole</a>
</td>
<td align="left" width="63%">
Gets the accessibility role for a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96eaac9c-7fab-4326-a737-4819794a34c6">OnGetDefaultAccessibilityAction</a>
</td>
<td align="left" width="63%">
Gets the default accessibility action for a Shell item.

</td>
</tr>
</table> 


## -remarks



This interface is used only by <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> (CLSID_NameSpaceTreeControl).
           




## -see-also




<a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a>
 

 

