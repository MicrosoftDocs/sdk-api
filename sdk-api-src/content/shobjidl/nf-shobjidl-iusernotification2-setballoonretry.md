---
UID: NF:shobjidl.IUserNotification2.SetBalloonRetry
title: IUserNotification2::SetBalloonRetry (shobjidl.h)
description: Specifies the conditions for trying to display user information when the first attempt fails. (IUserNotification2.SetBalloonRetry)
helpviewer_keywords: ["IUserNotification2 interface [Windows Shell]","SetBalloonRetry method","IUserNotification2.SetBalloonRetry","IUserNotification2::SetBalloonRetry","SetBalloonRetry","SetBalloonRetry method [Windows Shell]","SetBalloonRetry method [Windows Shell]","IUserNotification2 interface","_shell_IUserNotification2_SetBalloonRetry","shell.IUserNotification2_SetBalloonRetry","shobjidl/IUserNotification2::SetBalloonRetry"]
old-location: shell\IUserNotification2_SetBalloonRetry.htm
tech.root: shell
ms.assetid: D6A72D9F-108F-4eaf-A867-F81C86C08809
ms.date: 12/05/2018
ms.keywords: IUserNotification2 interface [Windows Shell],SetBalloonRetry method, IUserNotification2.SetBalloonRetry, IUserNotification2::SetBalloonRetry, SetBalloonRetry, SetBalloonRetry method [Windows Shell], SetBalloonRetry method [Windows Shell],IUserNotification2 interface, _shell_IUserNotification2_SetBalloonRetry, shell.IUserNotification2_SetBalloonRetry, shobjidl/IUserNotification2::SetBalloonRetry
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
 - IUserNotification2::SetBalloonRetry
 - shobjidl/IUserNotification2::SetBalloonRetry
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
 - IUserNotification2.SetBalloonRetry
---

# IUserNotification2::SetBalloonRetry


## -description

Specifies the conditions for trying to display user information when the first attempt fails.

## -parameters

### -param dwShowTime [in]

Type: <b>DWORD</b>

The amount of time, in milliseconds, to display the user information.

### -param dwInterval [in]

Type: <b>DWORD</b>

The interval of time, in milliseconds, between attempts to display the user information.

### -param cRetryCount [in]

Type: <b>UINT</b>

The number of times the system should try to display the user information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusernotification2">IUserNotification2</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-setballoonretry">SetBalloonRetry</a>
