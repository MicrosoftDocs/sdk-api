---
UID: NF:shobjidl.IUserAccountChangeCallback.OnPictureChange
title: IUserAccountChangeCallback::OnPictureChange (shobjidl.h)
description: Called to send notifications when the picture that represents a user account is changed.
helpviewer_keywords: ["IUserAccountChangeCallback interface [Windows Shell]","OnPictureChange method","IUserAccountChangeCallback.OnPictureChange","IUserAccountChangeCallback::OnPictureChange","OnPictureChange","OnPictureChange method [Windows Shell]","OnPictureChange method [Windows Shell]","IUserAccountChangeCallback interface","_shell_IUserAccountChangeCallback_OnPictureChange","shell.IUserAccountChangeCallback_OnPictureChange","shobjidl/IUserAccountChangeCallback::OnPictureChange"]
old-location: shell\IUserAccountChangeCallback_OnPictureChange.htm
tech.root: shell
ms.assetid: 9e524edc-3921-4fec-9999-4fd9f51f347b
ms.date: 12/05/2018
ms.keywords: IUserAccountChangeCallback interface [Windows Shell],OnPictureChange method, IUserAccountChangeCallback.OnPictureChange, IUserAccountChangeCallback::OnPictureChange, OnPictureChange, OnPictureChange method [Windows Shell], OnPictureChange method [Windows Shell],IUserAccountChangeCallback interface, _shell_IUserAccountChangeCallback_OnPictureChange, shell.IUserAccountChangeCallback_OnPictureChange, shobjidl/IUserAccountChangeCallback::OnPictureChange
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IUserAccountChangeCallback::OnPictureChange
 - shobjidl/IUserAccountChangeCallback::OnPictureChange
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
 - IUserAccountChangeCallback.OnPictureChange
---

# IUserAccountChangeCallback::OnPictureChange


## -description

Called to send notifications when the picture that represents a user account is changed.

## -parameters

### -param pszUserName [in]

Type: <b>LPCWSTR</b>

Pointer to a string that contains the user name. Set this parameter to <b>NULL</b> to specify the current user.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the picture that represents a user account changes, the callback object notifies all applications that are registered under this registry subkey:

<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>UserPictureChange</b></pre>

