---
UID: NN:shobjidl.IUserNotification2
title: IUserNotification2 (shobjidl.h)
description: Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.helpviewer_keywords: ["IUserNotification2","IUserNotification2 interface [Windows Shell]","IUserNotification2 interface [Windows Shell]","described","_shell_IUserNotification2","shell.IUserNotification2","shobjidl/IUserNotification2"]
old-location: shell\IUserNotification2.htm
tech.root: shell
ms.assetid: 6605a014-4f79-4856-8fd9-df926ea76052
ms.date: 12/05/2018
ms.keywords: IUserNotification2, IUserNotification2 interface [Windows Shell], IUserNotification2 interface [Windows Shell],described, _shell_IUserNotification2, shell.IUserNotification2, shobjidl/IUserNotification2
f1_keywords:
- shobjidl/IUserNotification2
dev_langs:
- c++
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
req.dll: Shell32.dll (version 6.0.6 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IUserNotification2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUserNotification2 interface


## -description


Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.
            
            
<div class="alert"><b>Note</b>  <b>IUserNotification2</b> does not inherit from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification">IUserNotification</a>. <b>IUserNotification2</b> differs from <b>IUserNotification</b> only in its <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-show">Show</a> method, which adds an additional parameter for a callback interface to communicate with the notification. Otherwise the two interfaces are identical in form and function. CLSID_UserNotification implements both versions of <b>Show</b> as an overload.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserNotification2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUserNotification2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserNotification2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-playsound">PlaySound</a>
</td>
<td align="left" width="63%">
Plays a sound in conjunction with the notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-setballooninfo">SetBalloonInfo</a>
</td>
<td align="left" width="63%">
Sets the information to be displayed in a balloon notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-setballoonretry">SetBalloonRetry</a>
</td>
<td align="left" width="63%">
Specifies the conditions for trying to display user information when the first attempt fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-seticoninfo">SetIconInfo</a>
</td>
<td align="left" width="63%">
Sets the notification area icon associated with specific user information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-show">Show</a>
</td>
<td align="left" width="63%">
Displays the user information in a balloon-style tooltip.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_UserNotification.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification">IUserNotification</a>
 

 

