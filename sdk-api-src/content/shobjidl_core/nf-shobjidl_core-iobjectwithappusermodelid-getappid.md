---
UID: NF:shobjidl_core.IObjectWithAppUserModelID.GetAppID
title: IObjectWithAppUserModelID::GetAppID
author: windows-sdk-content
description: Retrieves a file type handler's explicit Application User Model ID (AppUserModelID), if one has been declared.
old-location: shell\IObjectWithAppUserModelID_GetAppID.htm
old-project: shell
ms.assetid: da6c4799-fda9-43e5-86eb-91a40db5ab6c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetAppID, GetAppID method [Windows Shell], GetAppID method [Windows Shell],IObjectWithAppUserModelID interface, IObjectWithAppUserModelID interface [Windows Shell],GetAppID method, IObjectWithAppUserModelID.GetAppID, IObjectWithAppUserModelID::GetAppID, _shell_IObjectWithAppUserModelID_GetAppID, shell.IObjectWithAppUserModelID_GetAppID, shobjidl_core/IObjectWithAppUserModelID::GetAppID
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IObjectWithAppUserModelID.GetAppID
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can only retrieve an AppUserModelID explicitly set for the handler. If the handler did not register an explicit AppUserModelID and is relying on a system-assigned AppUserModelID, this method will not retrieve the AppUserModelID. For more information, see <a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/f5b4e6bf-a5bf-49c5-b343-e9c1ec6c263d">IObjectWithAppUserModelID</a>



<a href="https://msdn.microsoft.com/6f6850fc-2aa5-46fa-b237-82aafa844092">IObjectWithAppUserModelID::SetAppID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

