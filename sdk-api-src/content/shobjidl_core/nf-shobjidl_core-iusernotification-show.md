---
UID: NF:shobjidl_core.IUserNotification.Show
title: IUserNotification::Show (shobjidl_core.h)
author: windows-sdk-content
description: Displays the notification.
old-location: shell\IUserNotification_Show.htm
tech.root: shell
ms.assetid: 1f908581-9635-4090-9e52-1dfb9a206d38
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUserNotification interface [Windows Shell],Show method, IUserNotification.Show, IUserNotification::Show, Show, Show method [Windows Shell], Show method [Windows Shell],IUserNotification interface, inet_IUserNotification_Show, shell.IUserNotification_Show, shobjidl_core/IUserNotification::Show
ms.topic: method
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IUserNotification.Show
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUserNotification::Show


## -description


Displays the notification.


## -parameters




### -param pqc [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a>*</b>

An <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a> interface pointer, used to determine whether the notification display can continue or should stop (for example, if the user closes the notification). This value can be <b>NULL</b>.


### -param dwContinuePollInterval [in]

Type: <b>DWORD</b>

The length of time, in milliseconds, to display user information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is equivalent to calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-show">Show</a> with <i>pSink</i>=<b>NULL</b>.



