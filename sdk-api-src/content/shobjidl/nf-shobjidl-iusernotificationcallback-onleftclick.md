---
UID: NF:shobjidl.IUserNotificationCallback.OnLeftClick
title: IUserNotificationCallback::OnLeftClick
author: windows-sdk-content
description: Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.
old-location: shell\IUserNotificationCallback_OnLeftClick.htm
tech.root: shell
ms.assetid: 0202aace-94d6-4619-8838-eea0b174ffb6
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IUserNotificationCallback interface [Windows Shell],OnLeftClick method, IUserNotificationCallback.OnLeftClick, IUserNotificationCallback::OnLeftClick, OnLeftClick, OnLeftClick method [Windows Shell], OnLeftClick method [Windows Shell],IUserNotificationCallback interface, _shell_IUserNotificationCallback_OnLeftClick, shell.IUserNotificationCallback_OnLeftClick, shobjidl/IUserNotificationCallback::OnLeftClick
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotificationCallback.OnLeftClick
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUserNotificationCallback::OnLeftClick


## -description


Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.


## -parameters




### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

Takes a pointer to the <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure which, when the method returns, points to the position of the mouse in the screen space where the mouse click occurred.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



