---
UID: NN:shobjidl_core.IAssocHandler
title: IAssocHandler (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods for operations with a file association dialog box or menu.
old-location: shell\IAssocHandler.htm
tech.root: shell
ms.assetid: 5d5a107c-2c0e-4242-8f40-97421937167c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAssocHandler, IAssocHandler interface [Windows Shell], IAssocHandler interface [Windows Shell],described, _shell_IAssocHandler, shell.IAssocHandler, shobjidl_core/IAssocHandler
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IAssocHandler"
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
 - IAssocHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssocHandler interface


## -description


Exposes methods for operations with a file association dialog box or menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssocHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAssocHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAssocHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-createinvoker">CreateInvoker</a>
</td>
<td align="left" width="63%">
Retrieves an object that enables the invocation of the associated handler on the current selection.  The invoker includes the ability to verify whether the current selection is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-geticonlocation">GetIconLocation</a>
</td>
<td align="left" width="63%">
Retrieves the location of the icon associated with the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the full path and file name of the executable file associated with the file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-getuiname">GetUIName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of an application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Directly invokes the associated handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-isrecommended">IsRecommended</a>
</td>
<td align="left" width="63%">
Indicates whether the application is registered as a recommended handler for the queried file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-makedefault">MakeDefault</a>
</td>
<td align="left" width="63%">
Sets an application as the default application for this file type.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker">IAssocHandlerInvoker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers">IEnumAssocHandlers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers">SHAssocEnumHandlers</a>
 

 

