---
UID: NN:shobjidl_core.IQueryContinue
title: IQueryContinue (shobjidl_core.h)
author: windows-sdk-content
description: Exposes a method that provides a simple, standard mechanism for objects to query a client for permission to continue an operation.
old-location: shell\IQueryContinue.htm
tech.root: shell
ms.assetid: 94dee6cc-a142-4180-a562-14f4ded16884
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IQueryContinue, IQueryContinue interface [Windows Shell], IQueryContinue interface [Windows Shell],described, inet_IQueryContinue, shell.IQueryContinue, shobjidl_core/IQueryContinue
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IQueryContinue"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryContinue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQueryContinue interface


## -description


Exposes a method that provides a simple, standard mechanism for objects to query a client for permission to continue an operation. Clients of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification">IUserNotification</a>, for example, must pass an implementation of <b>IQueryContinue</b> to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show">IUserNotification::Show</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryContinue</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryContinue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueryContinue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue">QueryContinue</a>
</td>
<td align="left" width="63%">
Returns S_OK if the operation associated with the current instance of this interface should continue.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification">IUserNotification</a>
 

 

