---
UID: NF:shobjidl_core.ILaunchSourceAppUserModelId.GetAppUserModelId
title: ILaunchSourceAppUserModelId::GetAppUserModelId (shobjidl_core.h)
author: windows-sdk-content
description: Retrieves an AppUserModelId from the source application.
old-location: shell\ILaunchSourceAppUserModelId_GetAppUserModelId.htm
tech.root: shell
ms.assetid: 1B5E57E2-6870-4A52-BA61-3113385F03F5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAppUserModelId, GetAppUserModelId method [Windows Shell], GetAppUserModelId method [Windows Shell],ILaunchSourceAppUserModelId interface, ILaunchSourceAppUserModelId interface [Windows Shell],GetAppUserModelId method, ILaunchSourceAppUserModelId.GetAppUserModelId, ILaunchSourceAppUserModelId::GetAppUserModelId, shell.ILaunchSourceAppUserModelId_GetAppUserModelId, shobjidl_core/ILaunchSourceAppUserModelId::GetAppUserModelId
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ILaunchSourceAppUserModelId.GetAppUserModelId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILaunchSourceAppUserModelId::GetAppUserModelId


## -description


Retrieves an <a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">AppUserModelId</a> from the source application.


## -parameters




### -param launchingApp [out]

Type: <b>LPWSTR*</b>

Contains a  pointer to a string that contains the <a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">AppUserModelId</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">AppUserModelId</a>



<a href="https://msdn.microsoft.com/B53325C9-DC89-4411-82D9-247C28AFB177">ILaunchSourceAppUserModelId</a>
 

 

