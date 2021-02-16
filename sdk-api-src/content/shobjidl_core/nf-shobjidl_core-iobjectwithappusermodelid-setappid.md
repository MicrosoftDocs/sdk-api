---
UID: NF:shobjidl_core.IObjectWithAppUserModelID.SetAppID
title: IObjectWithAppUserModelID::SetAppID (shobjidl_core.h)
description: Specifies a unique application-defined Application User Model ID (AppUserModelID) that identifies the object as a handler for a specific file type. This method is used by applications that require dynamic AppUserModelIDs.
helpviewer_keywords: ["IObjectWithAppUserModelID interface [Windows Shell]","SetAppID method","IObjectWithAppUserModelID.SetAppID","IObjectWithAppUserModelID::SetAppID","SetAppID","SetAppID method [Windows Shell]","SetAppID method [Windows Shell]","IObjectWithAppUserModelID interface","_shell_IObjectWithAppUserModelID_SetAppID","shell.IObjectWithAppUserModelID_SetAppID","shobjidl_core/IObjectWithAppUserModelID::SetAppID"]
old-location: shell\IObjectWithAppUserModelID_SetAppID.htm
tech.root: shell
ms.assetid: 6f6850fc-2aa5-46fa-b237-82aafa844092
ms.date: 12/05/2018
ms.keywords: IObjectWithAppUserModelID interface [Windows Shell],SetAppID method, IObjectWithAppUserModelID.SetAppID, IObjectWithAppUserModelID::SetAppID, SetAppID, SetAppID method [Windows Shell], SetAppID method [Windows Shell],IObjectWithAppUserModelID interface, _shell_IObjectWithAppUserModelID_SetAppID, shell.IObjectWithAppUserModelID_SetAppID, shobjidl_core/IObjectWithAppUserModelID::SetAppID
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectWithAppUserModelID::SetAppID
 - shobjidl_core/IObjectWithAppUserModelID::SetAppID
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
 - IObjectWithAppUserModelID.SetAppID
---

# IObjectWithAppUserModelID::SetAppID


## -description

Specifies a unique application-defined Application User Model ID (AppUserModelID) that identifies the object as a handler for a specific file type. This method is used by applications that require dynamic AppUserModelIDs.

## -parameters

### -param pszAppID [in]

Type: <b>LPCWSTR</b>

A pointer to the AppUserModelID string to assign to an application.

## -returns

Type: <b>HRESULT</b>

Custom implementations that do not require dynamic AppUserModelIDs can return E_NOTIMPL. Custom implementations that require dynamic AppUserModelIDs should return S_OK if successful, or an error value otherwise.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid">IObjectWithAppUserModelID</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithappusermodelid-getappid">IObjectWithAppUserModelID::GetAppID</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid">SetCurrentProcessExplicitAppUserModelID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>