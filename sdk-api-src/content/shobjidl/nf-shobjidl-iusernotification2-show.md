---
UID: NF:shobjidl.IUserNotification2.Show
title: IUserNotification2::Show (shobjidl.h)
description: Displays the user information in a balloon-style tooltip.
helpviewer_keywords: ["IUserNotification2 interface [Windows Shell]","Show method","IUserNotification2.Show","IUserNotification2::Show","Show","Show method [Windows Shell]","Show method [Windows Shell]","IUserNotification2 interface","_shell_IUserNotification2_Show","shell.IUserNotification2_Show","shobjidl/IUserNotification2::Show"]
old-location: shell\IUserNotification2_Show.htm
tech.root: shell
ms.assetid: 928e9a78-6976-4dcb-b01d-766561f6a861
ms.date: 12/05/2018
ms.keywords: IUserNotification2 interface [Windows Shell],Show method, IUserNotification2.Show, IUserNotification2::Show, Show, Show method [Windows Shell], Show method [Windows Shell],IUserNotification2 interface, _shell_IUserNotification2_Show, shell.IUserNotification2_Show, shobjidl/IUserNotification2::Show
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserNotification2::Show
 - shobjidl/IUserNotification2::Show
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotification2.Show
---

# IUserNotification2::Show


## -description

Displays the user information in a balloon-style tooltip.

## -parameters

### -param pqc [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a> interface pointer, used to determine whether the notification display can continue or should stop (for example, if the user closes the notification). This value can be <b>NULL</b>.

### -param dwContinuePollInterval [in]

Type: <b>DWORD</b>

The length of time, in milliseconds, to display user information.

### -param pSink [in]

Type: <b><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusernotificationcallback">IUserNotificationCallback</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusernotificationcallback">IUserNotificationCallback</a> interface, used to handle mouse click and hover actions on the notification area icon and within the notification itself. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusernotification2">IUserNotification2</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show">Show</a>