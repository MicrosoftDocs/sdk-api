---
UID: NF:shobjidl_core.IObjectWithAppUserModelID.SetAppID
title: IObjectWithAppUserModelID::SetAppID
author: windows-sdk-content
description: Specifies a unique application-defined Application User Model ID (AppUserModelID) that identifies the object as a handler for a specific file type. This method is used by applications that require dynamic AppUserModelIDs.
old-location: shell\IObjectWithAppUserModelID_SetAppID.htm
tech.root: shell
ms.assetid: 6f6850fc-2aa5-46fa-b237-82aafa844092
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IObjectWithAppUserModelID interface [Windows Shell],SetAppID method, IObjectWithAppUserModelID.SetAppID, IObjectWithAppUserModelID::SetAppID, SetAppID, SetAppID method [Windows Shell], SetAppID method [Windows Shell],IObjectWithAppUserModelID interface, _shell_IObjectWithAppUserModelID_SetAppID, shell.IObjectWithAppUserModelID_SetAppID, shobjidl_core/IObjectWithAppUserModelID::SetAppID
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IObjectWithAppUserModelID.SetAppID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/f5b4e6bf-a5bf-49c5-b343-e9c1ec6c263d">IObjectWithAppUserModelID</a>



<a href="https://msdn.microsoft.com/da6c4799-fda9-43e5-86eb-91a40db5ab6c">IObjectWithAppUserModelID::GetAppID</a>



<a href="https://msdn.microsoft.com/2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c">SetCurrentProcessExplicitAppUserModelID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

