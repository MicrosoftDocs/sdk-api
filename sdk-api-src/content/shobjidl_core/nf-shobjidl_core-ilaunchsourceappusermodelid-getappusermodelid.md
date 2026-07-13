---
UID: NF:shobjidl_core.ILaunchSourceAppUserModelId.GetAppUserModelId
title: ILaunchSourceAppUserModelId::GetAppUserModelId (shobjidl_core.h)
description: Retrieves an AppUserModelId from the source application.
helpviewer_keywords: ["GetAppUserModelId","GetAppUserModelId method [Windows Shell]","GetAppUserModelId method [Windows Shell]","ILaunchSourceAppUserModelId interface","ILaunchSourceAppUserModelId interface [Windows Shell]","GetAppUserModelId method","ILaunchSourceAppUserModelId.GetAppUserModelId","ILaunchSourceAppUserModelId::GetAppUserModelId","shell.ILaunchSourceAppUserModelId_GetAppUserModelId","shobjidl_core/ILaunchSourceAppUserModelId::GetAppUserModelId"]
old-location: shell\ILaunchSourceAppUserModelId_GetAppUserModelId.htm
tech.root: shell
ms.assetid: 1B5E57E2-6870-4A52-BA61-3113385F03F5
ms.date: 12/05/2018
ms.keywords: GetAppUserModelId, GetAppUserModelId method [Windows Shell], GetAppUserModelId method [Windows Shell],ILaunchSourceAppUserModelId interface, ILaunchSourceAppUserModelId interface [Windows Shell],GetAppUserModelId method, ILaunchSourceAppUserModelId.GetAppUserModelId, ILaunchSourceAppUserModelId::GetAppUserModelId, shell.ILaunchSourceAppUserModelId_GetAppUserModelId, shobjidl_core/ILaunchSourceAppUserModelId::GetAppUserModelId
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILaunchSourceAppUserModelId::GetAppUserModelId
 - shobjidl_core/ILaunchSourceAppUserModelId::GetAppUserModelId
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
 - ILaunchSourceAppUserModelId.GetAppUserModelId
---

# ILaunchSourceAppUserModelId::GetAppUserModelId


## -description

Retrieves an <a href="/windows/desktop/shell/appids">AppUserModelId</a> from the source application.

## -parameters

### -param launchingApp [out]

Type: <b>LPWSTR*</b>

Contains a  pointer to a string that contains the <a href="/windows/desktop/shell/appids">AppUserModelId</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/appids">AppUserModelId</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid">ILaunchSourceAppUserModelId</a>