---
UID: NN:shobjidl.IUserNotificationCallback
title: IUserNotificationCallback
author: windows-sdk-content
description: Exposes a method for the handling of a mouse click or shortcut menu access in a notification balloon. Used with IUserNotification2::Show.
old-location: shell\IUserNotificationCallback.htm
old-project: shell
ms.assetid: f746a4d4-8649-43a1-ac9b-773402dfb6c7
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IUserNotificationCallback, IUserNotificationCallback interface [Windows Shell], IUserNotificationCallback interface [Windows Shell],described, _shell_IUserNotificationCallback, shell.IUserNotificationCallback, shobjidl/IUserNotificationCallback
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotificationCallback
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Shell32.dll (version 6.0.6 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserNotificationCallback interface


## -description


Exposes a method for the handling of a mouse click or shortcut menu access in a notification balloon. Used with <a href="https://msdn.microsoft.com/928e9a78-6976-4dcb-b01d-766561f6a861">IUserNotification2::Show</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserNotificationCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUserNotificationCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserNotificationCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7360a2b-30ed-459e-ab6d-56a2127c2668">OnBalloonUserClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks the balloon. The application may respond with an action that is suitable for the balloon being clicked.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb0b1de0-a42c-4789-aac0-885a574f89f6">OnContextMenu</a>
</td>
<td align="left" width="63%">
Called when the user right-clicks (or presses SHIFT+F10) the icon in the notification area. The application should show its context menu in response.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0202aace-94d6-4619-8838-eea0b174ffb6">OnLeftClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.

</td>
</tr>
</table> 

