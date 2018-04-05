---
UID: NF:shobjidl.IUserNotificationCallback.OnLeftClick
title: IUserNotificationCallback::OnLeftClick method
author: windows-driver-content
description: Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.
old-location: shell\IUserNotificationCallback_OnLeftClick.htm
old-project: shell
ms.assetid: 0202aace-94d6-4619-8838-eea0b174ffb6
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IUserNotificationCallback, IUserNotificationCallback interface [Windows Shell], OnLeftClick method, IUserNotificationCallback::OnLeftClick, OnLeftClick method [Windows Shell], OnLeftClick method [Windows Shell], IUserNotificationCallback interface, OnLeftClick,IUserNotificationCallback.OnLeftClick, _shell_IUserNotificationCallback_OnLeftClick, shell.IUserNotificationCallback_OnLeftClick, shobjidl/IUserNotificationCallback::OnLeftClick
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	Shobjidl.h
api_name:
-	IUserNotificationCallback.OnLeftClick
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserNotificationCallback::OnLeftClick method


## -description


Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.


## -parameters




### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

Takes a pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure which, when the method returns, points to the position of the mouse in the screen space where the mouse click occurred.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



