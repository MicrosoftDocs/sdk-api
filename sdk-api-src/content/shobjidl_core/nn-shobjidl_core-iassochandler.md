---
UID: NN:shobjidl_core.IAssocHandler
title: IAssocHandler
author: windows-sdk-content
description: Exposes methods for operations with a file association dialog box or menu.
old-location: shell\IAssocHandler.htm
old-project: shell
ms.assetid: 5d5a107c-2c0e-4242-8f40-97421937167c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAssocHandler, IAssocHandler interface [Windows Shell], IAssocHandler interface [Windows Shell],described, _shell_IAssocHandler, shell.IAssocHandler, shobjidl_core/IAssocHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAssocHandler
product: Windows
targetos: Windows
req.lib: Twinapi.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAssocHandler interface


## -description


Exposes methods for operations with a file association dialog box or menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssocHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAssocHandler</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12ffd2f1-e041-41f1-9b57-282a166ccbf7">CreateInvoker</a>
</td>
<td align="left" width="63%">
Retrieves an object that enables the invocation of the associated handler on the current selection.  The invoker includes the ability to verify whether the current selection is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b883c2c-6845-4e53-b41b-83c09091ee53">GetIconLocation</a>
</td>
<td align="left" width="63%">
Retrieves the location of the icon associated with the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d20aee32-fa5a-40a9-b0e2-8479a90fcf35">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the full path and file name of the executable file associated with the file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf714cf9-a16a-40a4-8dd8-c53c289967f5">GetUIName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of an application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d22c987-3a25-4a36-8411-eaed921d066e">Invoke</a>
</td>
<td align="left" width="63%">
Directly invokes the associated handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c312db3-a656-436c-a012-669553355fa5">IsRecommended</a>
</td>
<td align="left" width="63%">
Indicates whether the application is registered as a recommended handler for the queried file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/106ac493-bde6-4327-b3be-3132bfd47415">MakeDefault</a>
</td>
<td align="left" width="63%">
Sets an application as the default application for this file type.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b602280e-4237-4539-9a10-cec21c65e90d">IAssocHandlerInvoker</a>



<a href="https://msdn.microsoft.com/c8b11157-4d00-4ab1-aea5-ce8ae35c43ce">IEnumAssocHandlers</a>



<a href="https://msdn.microsoft.com/83db466b-e00c-4015-879f-c5c222f45b8c">SHAssocEnumHandlers</a>
 

 

