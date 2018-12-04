---
UID: NN:shobjidl_core.IUserNotification
title: IUserNotification
author: windows-sdk-content
description: Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.
old-location: shell\IUserNotification.htm
tech.root: shell
ms.assetid: 24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IUserNotification, IUserNotification interface [Windows Shell], IUserNotification interface [Windows Shell],described, inet_IUserNotification, shell.IUserNotification, shobjidl_core/IUserNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUserNotification interface


## -description


Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.

            
<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/6605a014-4f79-4856-8fd9-df926ea76052">IUserNotification2</a> differs from <b>IUserNotification</b> only in its <a href="https://msdn.microsoft.com/928e9a78-6976-4dcb-b01d-766561f6a861">Show</a> method, which adds an additional parameter for a callback interface to communicate with the notification. Otherwise the two interfaces are identical in form and function. CLSID_UserNotification implements both versions of <b>Show</b> as an overload.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserNotification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUserNotification</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3d7533c8-3b52-42dd-bfaa-2305bf3b0b18">PlaySound</a>
</td>
<td align="left" width="63%">
Plays a sound in conjunction with the notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd782a4b-fe3c-419b-ad55-ea3faf12e628">SetBalloonInfo</a>
</td>
<td align="left" width="63%">
Sets the information to be displayed in a balloon notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9ad42e1-19eb-44a9-aa09-4a31840104d6">SetBalloonRetry</a>
</td>
<td align="left" width="63%">
Specifies the conditions for trying to display user information when the first attempt fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9a3612e-8a25-48d5-8122-44d6aa217bab">SetIconInfo</a>
</td>
<td align="left" width="63%">
Sets the notification area icon associated with specific user information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f908581-9635-4090-9e52-1dfb9a206d38">Show</a>
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




<a href="https://msdn.microsoft.com/6605a014-4f79-4856-8fd9-df926ea76052">IUserNotification2</a>
 

 

