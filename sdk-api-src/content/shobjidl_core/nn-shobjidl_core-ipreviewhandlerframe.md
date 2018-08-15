---
UID: NN:shobjidl_core.IPreviewHandlerFrame
title: IPreviewHandlerFrame
author: windows-sdk-content
description: Enables preview handlers to pass keyboard shortcuts to the host. This interface retrieves a list of keyboard shortcuts and directs the host to handle a keyboard shortcut.
old-location: shell\IPreviewHandlerFrame.htm
old-project: shell
ms.assetid: 4e1316e5-f736-4a9b-887b-ddc48a615c42
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPreviewHandlerFrame, IPreviewHandlerFrame interface [Windows Shell], IPreviewHandlerFrame interface [Windows Shell],described, _shell_IPreviewHandlerFrame, shell.IPreviewHandlerFrame, shobjidl_core/IPreviewHandlerFrame
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.redist: Windows Search 4 or later
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - IPreviewHandlerFrame
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IPreviewHandlerFrame interface


## -description


Enables preview handlers to pass keyboard shortcuts to the host. This interface retrieves a list of keyboard shortcuts and directs the host to handle a keyboard shortcut.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPreviewHandlerFrame</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPreviewHandlerFrame</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPreviewHandlerFrame</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/953b7571-0da1-4e31-bb6f-1761f8103c6e">GetWindowContext</a>
</td>
<td align="left" width="63%">
Gets a list of the keyboard shortcuts for the preview host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Directs the host to handle an keyboard shortcut passed from the preview handler.

</td>
</tr>
</table> 


## -remarks



This is an interface that preview handlers use to communicate keyboard shortcuts to the host. Preview handlers obtain this interface by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the pointer passed as a parameter to <a href="https://msdn.microsoft.com/5e95b2a6-85b3-4899-9e23-54ed9e69e821">SetSite</a>. Preview handlers do not need to implement this interface.



