---
UID: NN:shobjidl_core.IUserNotification
title: IUserNotification (shobjidl_core.h)
description: Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.
helpviewer_keywords: ["IUserNotification","IUserNotification interface [Windows Shell]","IUserNotification interface [Windows Shell]","described","inet_IUserNotification","shell.IUserNotification","shobjidl_core/IUserNotification"]
old-location: shell\IUserNotification.htm
tech.root: shell
ms.assetid: 24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad
ms.date: 12/05/2018
ms.keywords: IUserNotification, IUserNotification interface [Windows Shell], IUserNotification interface [Windows Shell],described, inet_IUserNotification, shell.IUserNotification, shobjidl_core/IUserNotification
f1_keywords:
- shobjidl_core/IUserNotification
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IUserNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUserNotification interface


## -description


Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.

            
<div class="alert"><b>Note</b>  <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iusernotification2">IUserNotification2</a> differs from <b>IUserNotification</b> only in its <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-show">Show</a> method, which adds an additional parameter for a callback interface to communicate with the notification. Otherwise the two interfaces are identical in form and function. CLSID_UserNotification implements both versions of <b>Show</b> as an overload.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserNotification</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUserNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-playsound">PlaySound</a>
</td>
<td align="left" width="63%">
Plays a sound in conjunction with the notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-setballooninfo">SetBalloonInfo</a>
</td>
<td align="left" width="63%">
Sets the information to be displayed in a balloon notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-setballoonretry">SetBalloonRetry</a>
</td>
<td align="left" width="63%">
Specifies the conditions for trying to display user information when the first attempt fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-seticoninfo">SetIconInfo</a>
</td>
<td align="left" width="63%">
Sets the notification area icon associated with specific user information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show">Show</a>
</td>
<td align="left" width="63%">
Displays the notification.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_UserNotification.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iusernotification2">IUserNotification2</a>
 

 

