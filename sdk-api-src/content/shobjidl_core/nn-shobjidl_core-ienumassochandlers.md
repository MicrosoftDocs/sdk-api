---
UID: NN:shobjidl_core.IEnumAssocHandlers
title: IEnumAssocHandlers (shobjidl_core.h)
description: Exposes a method that allows enumeration of a collection of handlers associated with particular file name extensions.
helpviewer_keywords: ["IEnumAssocHandlers","IEnumAssocHandlers interface [Windows Shell]","IEnumAssocHandlers interface [Windows Shell]","described","_shell_IEnumAssocHandlers","shell.IEnumAssocHandlers","shobjidl_core/IEnumAssocHandlers"]
old-location: shell\IEnumAssocHandlers.htm
tech.root: shell
ms.assetid: c8b11157-4d00-4ab1-aea5-ce8ae35c43ce
ms.date: 12/05/2018
ms.keywords: IEnumAssocHandlers, IEnumAssocHandlers interface [Windows Shell], IEnumAssocHandlers interface [Windows Shell],described, _shell_IEnumAssocHandlers, shell.IEnumAssocHandlers, shobjidl_core/IEnumAssocHandlers
f1_keywords:
- shobjidl_core/IEnumAssocHandlers
dev_langs:
- c++
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
- IEnumAssocHandlers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAssocHandlers interface


## -description


Exposes a method that allows enumeration of a collection of handlers associated with particular file name extensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAssocHandlers</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumAssocHandlers</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAssocHandlers</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumassochandlers-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of elements.

</td>
</tr>
</table> 


## -remarks




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers">SHAssocEnumHandlers</a> is the usual method of creating an IEnumAssocHandlers pointer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker">IAssocHandlerInvoker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers">SHAssocEnumHandlers</a>
 

 

