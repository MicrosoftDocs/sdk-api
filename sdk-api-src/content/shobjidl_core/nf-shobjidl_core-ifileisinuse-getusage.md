---
UID: NF:shobjidl_core.IFileIsInUse.GetUsage
title: IFileIsInUse::GetUsage (shobjidl_core.h)
description: Gets a value that indicates how the file in use is being used.
helpviewer_keywords: ["GetUsage","GetUsage method [Windows Shell]","GetUsage method [Windows Shell]","IFileIsInUse interface","IFileIsInUse interface [Windows Shell]","GetUsage method","IFileIsInUse.GetUsage","IFileIsInUse::GetUsage","_shell_IFileIsInUse_GetUsage","shell.IFileIsInUse_GetUsage","shobjidl_core/IFileIsInUse::GetUsage"]
old-location: shell\IFileIsInUse_GetUsage.htm
tech.root: shell
ms.assetid: 7baba34d-b246-4d48-9f0c-e950d33ed5cf
ms.date: 12/05/2018
ms.keywords: GetUsage, GetUsage method [Windows Shell], GetUsage method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetUsage method, IFileIsInUse.GetUsage, IFileIsInUse::GetUsage, _shell_IFileIsInUse_GetUsage, shell.IFileIsInUse_GetUsage, shobjidl_core/IFileIsInUse::GetUsage
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
 - IFileIsInUse::GetUsage
 - shobjidl_core/IFileIsInUse::GetUsage
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
 - IFileIsInUse.GetUsage
---

# IFileIsInUse::GetUsage


## -description

Gets a value that indicates how the file in use is being used.

## -parameters

### -param pfut [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type">FILE_USAGE_TYPE</a>*</b>

Pointer to a value that, when this method returns successfully, receives one of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type">FILE_USAGE_TYPE</a> values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.