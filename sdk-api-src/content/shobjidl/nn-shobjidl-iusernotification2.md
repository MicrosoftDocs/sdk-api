---
UID: NN:shobjidl.IUserNotification2
title: IUserNotification2
author: windows-driver-content
description: Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.
old-location: shell\IUserNotification2.htm
old-project: shell
ms.assetid: 6605a014-4f79-4856-8fd9-df926ea76052
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IUserNotification2, IUserNotification2 interface [Windows Shell], IUserNotification2 interface [Windows Shell],described, _shell_IUserNotification2, shell.IUserNotification2, shobjidl/IUserNotification2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IUserNotification2
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Shell32.dll (version 6.0.6 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserNotification2 interface


## -description


Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.
            
            
<div class="alert"><b>Note</b>  <b>IUserNotification2</b> does not inherit from <a href="https://msdn.microsoft.com/24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad">IUserNotification</a>. <b>IUserNotification2</b> differs from <b>IUserNotification</b> only in its <a href="https://msdn.microsoft.com/928e9a78-6976-4dcb-b01d-766561f6a861">Show</a> method, which adds an additional parameter for a callback interface to communicate with the notification. Otherwise the two interfaces are identical in form and function. CLSID_UserNotification implements both versions of <b>Show</b> as an overload.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserNotification2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUserNotification2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn965711">PlaySound</a>
</td>
<td align="left" width="63%">
Plays a sound in conjunction with the notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3615F243-1F1B-4b9f-9083-B1EF3B5048DD">SetBalloonInfo</a>
</td>
<td align="left" width="63%">
Sets the information to be displayed in a balloon notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D6A72D9F-108F-4eaf-A867-F81C86C08809">SetBalloonRetry</a>
</td>
<td align="left" width="63%">
Specifies the conditions for trying to display user information when the first attempt fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9A7B5891-6A0C-4302-89F7-07D985B0F185">SetIconInfo</a>
</td>
<td align="left" width="63%">
Sets the notification area icon associated with specific user information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/928e9a78-6976-4dcb-b01d-766561f6a861">Show</a>
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




<a href="https://msdn.microsoft.com/24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad">IUserNotification</a>
 

 

