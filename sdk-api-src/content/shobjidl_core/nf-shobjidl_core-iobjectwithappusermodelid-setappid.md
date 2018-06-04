---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

