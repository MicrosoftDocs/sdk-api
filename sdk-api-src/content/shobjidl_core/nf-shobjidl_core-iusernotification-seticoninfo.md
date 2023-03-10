---
UID: NF:shobjidl_core.IUserNotification.SetIconInfo
title: IUserNotification::SetIconInfo (shobjidl_core.h)
description: Sets the notification area icon associated with specific user information. (IUserNotification.SetIconInfo)
helpviewer_keywords: ["IUserNotification interface [Windows Shell]","SetIconInfo method","IUserNotification.SetIconInfo","IUserNotification::SetIconInfo","SetIconInfo","SetIconInfo method [Windows Shell]","SetIconInfo method [Windows Shell]","IUserNotification interface","inet_IUserNotification_SetIconInfo","shell.IUserNotification_SetIconInfo","shobjidl_core/IUserNotification::SetIconInfo"]
old-location: shell\IUserNotification_SetIconInfo.htm
tech.root: shell
ms.assetid: f9a3612e-8a25-48d5-8122-44d6aa217bab
ms.date: 12/05/2018
ms.keywords: IUserNotification interface [Windows Shell],SetIconInfo method, IUserNotification.SetIconInfo, IUserNotification::SetIconInfo, SetIconInfo, SetIconInfo method [Windows Shell], SetIconInfo method [Windows Shell],IUserNotification interface, inet_IUserNotification_SetIconInfo, shell.IUserNotification_SetIconInfo, shobjidl_core/IUserNotification::SetIconInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserNotification::SetIconInfo
 - shobjidl_core/IUserNotification::SetIconInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IUserNotification.SetIconInfo
---

# IUserNotification::SetIconInfo


## -description

Sets the notification area icon associated with specific user information.

## -parameters

### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon.

### -param pszToolTip [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the tooltip text to display for the specified icon. This value can be <b>NULL</b>, although it is not recommended.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

