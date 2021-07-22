---
UID: NF:shobjidl_core.IFileIsInUse.GetAppName
title: IFileIsInUse::GetAppName (shobjidl_core.h)
description: Retrieves the name of the application that is using the file.
helpviewer_keywords: ["GetAppName","GetAppName method [Windows Shell]","GetAppName method [Windows Shell]","IFileIsInUse interface","IFileIsInUse interface [Windows Shell]","GetAppName method","IFileIsInUse.GetAppName","IFileIsInUse::GetAppName","_shell_IFileIsInUse_GetAppName","shell.IFileIsInUse_GetAppName","shobjidl_core/IFileIsInUse::GetAppName"]
old-location: shell\IFileIsInUse_GetAppName.htm
tech.root: shell
ms.assetid: 282334a9-28b4-4c3f-977e-824011efe381
ms.date: 12/05/2018
ms.keywords: GetAppName, GetAppName method [Windows Shell], GetAppName method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetAppName method, IFileIsInUse.GetAppName, IFileIsInUse::GetAppName, _shell_IFileIsInUse_GetAppName, shell.IFileIsInUse_GetAppName, shobjidl_core/IFileIsInUse::GetAppName
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IFileIsInUse::GetAppName
 - shobjidl_core/IFileIsInUse::GetAppName
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
 - IFileIsInUse.GetAppName
---

# IFileIsInUse::GetAppName


## -description

Retrieves the name of the application that is using the file.

## -parameters

### -param ppszName [out]

Type: <b>LPWSTR*</b>

The address of a pointer to a buffer that, when this method returns successfully, receives the application name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This information can be passed to the user in a dialog box so that the user knows the source of the conflict and can act accordingly. For instance "File.txt is in use by Litware."

