---
UID: NN:shobjidl_core.INamespaceWalkCB2
title: INamespaceWalkCB2 (shobjidl_core.h)
author: windows-sdk-content
description: Extends INamespaceWalkCB with a method that is required in order to complete a namespace walk. This method removes data collected during the walk.
old-location: shell\INamespaceWalkCB2.htm
tech.root: shell
ms.assetid: a748083b-a99e-4015-93da-112d2950f623
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INamespaceWalkCB2, INamespaceWalkCB2 interface [Windows Shell], INamespaceWalkCB2 interface [Windows Shell],described, _shell_INamespaceWalkCB2, shell.INamespaceWalkCB2, shobjidl_core/INamespaceWalkCB2
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/INamespaceWalkCB2"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - shobjidl_core.h
api_name:
 - INamespaceWalkCB2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INamespaceWalkCB2 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a> with a method that is required in order to complete a namespace walk. This method removes data collected during the walk.    


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamespaceWalkCB2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a>. <b>INamespaceWalkCB2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamespaceWalkCB2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb2-walkcomplete">WalkComplete</a>
</td>
<td align="left" width="63%">
Removes data collected during a namespace walk.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a> interface, from which it inherits.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a>
 

 

