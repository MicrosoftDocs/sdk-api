---
UID: NF:shobjidl.IUserNotification2.SetIconInfo
title: IUserNotification2::SetIconInfo (shobjidl.h)
description: Sets the notification area icon associated with specific user information. (IUserNotification2.SetIconInfo)
helpviewer_keywords: ["IUserNotification2 interface [Windows Shell]","SetIconInfo method","IUserNotification2.SetIconInfo","IUserNotification2::SetIconInfo","SetIconInfo","SetIconInfo method [Windows Shell]","SetIconInfo method [Windows Shell]","IUserNotification2 interface","_shell_IUserNotification2_SetIconInfo","shell.IUserNotification2_SetIconInfo","shobjidl/IUserNotification2::SetIconInfo"]
old-location: shell\IUserNotification2_SetIconInfo.htm
tech.root: shell
ms.assetid: 9A7B5891-6A0C-4302-89F7-07D985B0F185
ms.date: 12/05/2018
ms.keywords: IUserNotification2 interface [Windows Shell],SetIconInfo method, IUserNotification2.SetIconInfo, IUserNotification2::SetIconInfo, SetIconInfo, SetIconInfo method [Windows Shell], SetIconInfo method [Windows Shell],IUserNotification2 interface, _shell_IUserNotification2_SetIconInfo, shell.IUserNotification2_SetIconInfo, shobjidl/IUserNotification2::SetIconInfo
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
 - IUserNotification2::SetIconInfo
 - shobjidl/IUserNotification2::SetIconInfo
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
 - IUserNotification2.SetIconInfo
---

# IUserNotification2::SetIconInfo


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

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusernotification2">IUserNotification2</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-seticoninfo">SetIconInfo</a>
