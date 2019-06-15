---
UID: NN:shobjidl_core.IRemoteComputer
title: IRemoteComputer (shobjidl_core.h)
author: windows-sdk-content
description: Exposes a method that enumerates or initializes a namespace extension when it is invoked on a remote object. This interface is used, for example, to initialize the remote printers virtual folder.
old-location: shell\IRemoteComputer.htm
tech.root: shell
ms.assetid: a2137043-baee-496b-b3ad-45af5a6f123e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRemoteComputer, IRemoteComputer interface [Windows Shell], IRemoteComputer interface [Windows Shell],described, _win32_IRemoteComputer, shell.IRemoteComputer, shobjidl_core/IRemoteComputer
ms.topic: interface
f1_keywords: ["shobjidl_core/IRemoteComputer"]
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRemoteComputer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRemoteComputer interface


## -description


Exposes a method that enumerates or initializes a namespace extension when it is invoked on a remote object. This interface is used, for example, to initialize the remote printers virtual folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteComputer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRemoteComputer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRemoteComputer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iremotecomputer-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Used by Windows Explorer or Internet Explorer when it is initializing or enumerating a namespace extension invoked on a remote computer.

</td>
</tr>
</table> 


## -remarks



Implement <b>IRemoteComputer</b> when your namespace extension may be invoked on a remote computer.

You do not call this interface directly. <b>IRemoteComputer</b> is used by the operating system only when it has confirmed that your application is aware of this interface.



