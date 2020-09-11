---
UID: NN:shobjidl.IUserNotificationCallback
title: IUserNotificationCallback (shobjidl.h)
description: Exposes a method for the handling of a mouse click or shortcut menu access in a notification balloon. Used with IUserNotification2::Show.
helpviewer_keywords: ["IUserNotificationCallback","IUserNotificationCallback interface [Windows Shell]","IUserNotificationCallback interface [Windows Shell]","described","_shell_IUserNotificationCallback","shell.IUserNotificationCallback","shobjidl/IUserNotificationCallback"]
old-location: shell\IUserNotificationCallback.htm
tech.root: shell
ms.assetid: f746a4d4-8649-43a1-ac9b-773402dfb6c7
ms.date: 12/05/2018
ms.keywords: IUserNotificationCallback, IUserNotificationCallback interface [Windows Shell], IUserNotificationCallback interface [Windows Shell],described, _shell_IUserNotificationCallback, shell.IUserNotificationCallback, shobjidl/IUserNotificationCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserNotificationCallback
 - shobjidl/IUserNotificationCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotificationCallback
---

# IUserNotificationCallback interface


## -description

Exposes a method for the handling of a mouse click or shortcut menu access in a notification balloon. Used with <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-show">IUserNotification2::Show</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserNotificationCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUserNotificationCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotificationcallback-onballoonuserclick">OnBalloonUserClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks the balloon. The application may respond with an action that is suitable for the balloon being clicked.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotificationcallback-oncontextmenu">OnContextMenu</a>
</td>
<td align="left" width="63%">
Called when the user right-clicks (or presses SHIFT+F10) the icon in the notification area. The application should show its context menu in response.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotificationcallback-onleftclick">OnLeftClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.

</td>
</tr>
</table>

