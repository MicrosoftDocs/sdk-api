---
UID: NF:shobjidl.IUserNotificationCallback.OnBalloonUserClick
title: IUserNotificationCallback::OnBalloonUserClick
author: windows-sdk-content
description: Called when the user clicks the balloon. The application may respond with an action that is suitable for the balloon being clicked.
old-location: shell\IUserNotificationCallback_OnBalloonUserClick.htm
tech.root: shell
ms.assetid: b7360a2b-30ed-459e-ab6d-56a2127c2668
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IUserNotificationCallback interface [Windows Shell],OnBalloonUserClick method, IUserNotificationCallback.OnBalloonUserClick, IUserNotificationCallback::OnBalloonUserClick, OnBalloonUserClick, OnBalloonUserClick method [Windows Shell], OnBalloonUserClick method [Windows Shell],IUserNotificationCallback interface, _shell_IUserNotificationCallback_OnBalloonUserClick, shell.IUserNotificationCallback_OnBalloonUserClick, shobjidl/IUserNotificationCallback::OnBalloonUserClick
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
 - IUserNotificationCallback.OnBalloonUserClick
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUserNotificationCallback::OnBalloonUserClick


## -description


Called when the user clicks the balloon. The application may respond with an action that is suitable for the balloon being clicked.



## -parameters




### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

Takes a pointer to the <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure which, upon method return, points to the position of the mouse in screen space where the mouse click occurred.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



