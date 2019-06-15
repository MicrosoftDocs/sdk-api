---
UID: NN:shobjidl_core.ITransferDestination
title: ITransferDestination (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that create a destination Shell item for a copy or move operation. This interface is provided to allow more control over file operations by providing an ITransferDestination::Advise method.
old-location: shell\ITransferDestination.htm
tech.root: shell
ms.assetid: 8d0049e0-e227-40ae-a282-cdc17f227e24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITransferDestination, ITransferDestination interface [Windows Shell], ITransferDestination interface [Windows Shell],described, _shell_ITransferDestination, shell.ITransferDestination, shobjidl_core/ITransferDestination
ms.topic: interface
f1_keywords: ["shobjidl_core/ITransferDestination"]
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
 - ITransferDestination
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransferDestination interface


## -description


Exposes methods that create a destination Shell item for a copy or move operation. This interface is provided to allow more control over file operations by providing an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise">ITransferDestination::Advise</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransferDestination</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransferDestination</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransferDestination</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise">Advise</a>
</td>
<td align="left" width="63%">
Sets up an advisory connection for notifications on the status of file operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-createitem">CreateItem</a>
</td>
<td align="left" width="63%">
Creates the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a>
 

 

