---
UID: NF:shobjidl_core.IUserNotification.SetBalloonRetry
title: IUserNotification::SetBalloonRetry (shobjidl_core.h)
description: Specifies the conditions for trying to display user information when the first attempt fails. (IUserNotification.SetBalloonRetry)
helpviewer_keywords: ["IUserNotification interface [Windows Shell]","SetBalloonRetry method","IUserNotification.SetBalloonRetry","IUserNotification::SetBalloonRetry","SetBalloonRetry","SetBalloonRetry method [Windows Shell]","SetBalloonRetry method [Windows Shell]","IUserNotification interface","inet_IUserNotification_SetBalloonRetry","shell.IUserNotification_SetBalloonRetry","shobjidl_core/IUserNotification::SetBalloonRetry"]
old-location: shell\IUserNotification_SetBalloonRetry.htm
tech.root: shell
ms.assetid: b9ad42e1-19eb-44a9-aa09-4a31840104d6
ms.date: 12/05/2018
ms.keywords: IUserNotification interface [Windows Shell],SetBalloonRetry method, IUserNotification.SetBalloonRetry, IUserNotification::SetBalloonRetry, SetBalloonRetry, SetBalloonRetry method [Windows Shell], SetBalloonRetry method [Windows Shell],IUserNotification interface, inet_IUserNotification_SetBalloonRetry, shell.IUserNotification_SetBalloonRetry, shobjidl_core/IUserNotification::SetBalloonRetry
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserNotification::SetBalloonRetry
 - shobjidl_core/IUserNotification::SetBalloonRetry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IUserNotification.SetBalloonRetry
---

# IUserNotification::SetBalloonRetry


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

