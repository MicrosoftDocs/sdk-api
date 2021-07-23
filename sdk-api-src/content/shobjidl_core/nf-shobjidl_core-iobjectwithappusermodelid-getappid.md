---
UID: NF:shobjidl_core.IObjectWithAppUserModelID.GetAppID
title: IObjectWithAppUserModelID::GetAppID (shobjidl_core.h)
description: Retrieves a file type handler's explicit Application User Model ID (AppUserModelID), if one has been declared.
helpviewer_keywords: ["GetAppID","GetAppID method [Windows Shell]","GetAppID method [Windows Shell]","IObjectWithAppUserModelID interface","IObjectWithAppUserModelID interface [Windows Shell]","GetAppID method","IObjectWithAppUserModelID.GetAppID","IObjectWithAppUserModelID::GetAppID","_shell_IObjectWithAppUserModelID_GetAppID","shell.IObjectWithAppUserModelID_GetAppID","shobjidl_core/IObjectWithAppUserModelID::GetAppID"]
old-location: shell\IObjectWithAppUserModelID_GetAppID.htm
tech.root: shell
ms.assetid: da6c4799-fda9-43e5-86eb-91a40db5ab6c
ms.date: 12/05/2018
ms.keywords: GetAppID, GetAppID method [Windows Shell], GetAppID method [Windows Shell],IObjectWithAppUserModelID interface, IObjectWithAppUserModelID interface [Windows Shell],GetAppID method, IObjectWithAppUserModelID.GetAppID, IObjectWithAppUserModelID::GetAppID, _shell_IObjectWithAppUserModelID_GetAppID, shell.IObjectWithAppUserModelID_GetAppID, shobjidl_core/IObjectWithAppUserModelID::GetAppID
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
 - IObjectWithAppUserModelID::GetAppID
 - shobjidl_core/IObjectWithAppUserModelID::GetAppID
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
 - IObjectWithAppUserModelID.GetAppID
---

# IObjectWithAppUserModelID::GetAppID


## -description

Retrieves a file type handler's explicit Application User Model ID (AppUserModelID), if one has been declared.

## -parameters

### -param ppszAppID [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of the AppUserModelID string assigned to the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can only retrieve an AppUserModelID explicitly set for the handler. If the handler did not register an explicit AppUserModelID and is relying on a system-assigned AppUserModelID, this method will not retrieve the AppUserModelID. For more information, see <a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid">IObjectWithAppUserModelID</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithappusermodelid-setappid">IObjectWithAppUserModelID::SetAppID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>