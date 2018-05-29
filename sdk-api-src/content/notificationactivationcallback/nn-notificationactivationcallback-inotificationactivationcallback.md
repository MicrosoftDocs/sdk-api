---
UID: NN:notificationactivationcallback.INotificationActivationCallback
title: INotificationActivationCallback
author: windows-sdk-content
description: Receives notification messages when an app is triggered through a toast from the action center.
old-location: win32_tile_badge_notif\inotificationactivationcallback.htm
old-project: win32_tile_badge_notif
ms.assetid: 9DB90C47-6FFA-44CA-8D33-709DD8CDDA29
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: INotificationActivationCallback, INotificationActivationCallback interface, INotificationActivationCallback interface,described, notificationactivationcallback/INotificationActivationCallback, win32_tile_badge_notif.inotificationactivationcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: notificationactivationcallback.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NL_INTERFACE_OFFLOAD_ROD, *PNL_INTERFACE_OFFLOAD_ROD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	NotificationActivationCallback.h
api_name:
-	INotificationActivationCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INotificationActivationCallback interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Receives notification messages when an app is triggered through a toast from the action center.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INotificationActivationCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INotificationActivationCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INotificationActivationCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C366FE9F-D962-485F-B029-A96AA3358942">Activate</a>
</td>
<td align="left" width="63%">
Called when a user interacts with a toast in the action center.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/050E6944-6727-4632-85E8-8E68887D4786">Respond to toast activations</a>
 

 

