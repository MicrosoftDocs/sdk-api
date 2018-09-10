---
UID: NF:notificationactivationcallback.INotificationActivationCallback.Activate
title: INotificationActivationCallback::Activate
author: windows-sdk-content
description: Called when a user interacts with a toast in the action center.
old-location: win32_tile_badge_notif\inotificationactivationcallback_activate.htm
tech.root: win32_tile_badge_notif
ms.assetid: C366FE9F-D962-485F-B029-A96AA3358942
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Activate, Activate method, Activate method,INotificationActivationCallback interface, INotificationActivationCallback interface,Activate method, INotificationActivationCallback.Activate, INotificationActivationCallback::Activate, notificationactivationcallback/INotificationActivationCallback::Activate, win32_tile_badge_notif.inotificationactivationcallback_activate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - NotificationActivationCallback.h
api_name:
 - INotificationActivationCallback.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INotificationActivationCallback::Activate


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Called when a user interacts with a toast in the action center.


## -parameters




### -param appUserModelId [in]

The unique identifier representing your app to the notification platform.


### -param invokedArgs [in]

Arguments from the invoked button. <b>NULL</b> if the toast indicates the default activation and no launch arguments were specified in the XML payload.


### -param data [in]

The data from the input elements available on the notification toast.


### -param count [in]

The number of <i>data</i> elements.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In order for your app to respond to toasts in the action center, you need to override this method in your app. You also will need to create a shortcut on the start menu. For more information about how to respond to activation notifications, see <a href="https://msdn.microsoft.com/050E6944-6727-4632-85E8-8E68887D4786">Respond to toast activations</a>.

If your application uses non-interactive toasts, you can respond to those without using <i>invokedArgs</i> or <i>data</i>.

If you return a failure code, the activation will fail and the user can try again to activate your app.




## -see-also




<a href="https://msdn.microsoft.com/9DB90C47-6FFA-44CA-8D33-709DD8CDDA29">INotificationActivationCallback</a>



<a href="https://msdn.microsoft.com/050E6944-6727-4632-85E8-8E68887D4786">Respond to toast activations</a>
 

 

