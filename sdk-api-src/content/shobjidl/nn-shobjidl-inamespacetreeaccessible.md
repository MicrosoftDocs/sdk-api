---
UID: NN:shobjidl.INameSpaceTreeAccessible
title: INameSpaceTreeAccessible (shobjidl.h)
author: windows-sdk-content
description: Exposes methods that perform accessibility actions on a Shell item from a namespace tree control.
old-location: shell\INameSpaceTreeAccessible.htm
tech.root: shell
ms.assetid: b14dfe40-e21a-4208-835f-e0febef60783
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeAccessible, INameSpaceTreeAccessible interface [Windows Shell], INameSpaceTreeAccessible interface [Windows Shell],described, _shell_INameSpaceTreeAccessible, shell.INameSpaceTreeAccessible, shobjidl/INameSpaceTreeAccessible
ms.topic: interface
f1_keywords: 
 - "shobjidl/INameSpaceTreeAccessible"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeAccessible interface


## -description


Exposes methods that perform accessibility actions on a Shell item from a namespace tree control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeAccessible</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INameSpaceTreeAccessible</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreeaccessible-ondodefaultaccessibilityaction">OnDoDefaultAccessibilityAction</a>
</td>
<td align="left" width="63%">
Invokes the default accessibility action on a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreeaccessible-ongetaccessibilityrole">OnGetAccessibilityRole</a>
</td>
<td align="left" width="63%">
Gets the accessibility role for a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreeaccessible-ongetdefaultaccessibilityaction">OnGetDefaultAccessibilityAction</a>
</td>
<td align="left" width="63%">
Gets the default accessibility action for a Shell item.

</td>
</tr>
</table> 


## -remarks



This interface is used only by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> (CLSID_NameSpaceTreeControl).
           




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a>
 

 

