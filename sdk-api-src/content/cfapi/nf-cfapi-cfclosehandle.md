---
UID: NF:cfapi.CfCloseHandle
title: CfCloseHandle function (cfapi.h)
description: Closes the file or directory handle returned by CfOpenFileWithOplock. This should not be used with standard Win32 file handles, only on handles used within CfApi.h.
helpviewer_keywords: ["CfCloseHandle","CfCloseHandle function","cfapi/CfCloseHandle","cloudApi.cfclosehandle"]
old-location: cloudapi\cfclosehandle.htm
tech.root: cloudapi
ms.assetid: ECBEF685-0769-4AEA-8A0F-D5FBB70CBB09
ms.date: 02/27/2023
ms.keywords: CfCloseHandle, CfCloseHandle function, cfapi/CfCloseHandle, cloudApi.cfclosehandle
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfCloseHandle
 - cfapi/CfCloseHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfCloseHandle
---

# CfCloseHandle function

## -description

Closes the file or directory handle returned by [CfOpenFileWithOplock](/windows/win32/api/cfapi/nf-cfapi-cfopenfilewithoplock). This should not be used with standard Win32 file handles, only on handles used within `CfApi.h`.

## -parameters

### -param FileHandle [in]

The file or directory handle to be closed.

## -see-also

[CfOpenFileWithOplock](/windows/win32/api/cfapi/nf-cfapi-cfopenfilewithoplock)
