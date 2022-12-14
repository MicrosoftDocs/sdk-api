---
UID: NF:cfapi.CfOpenFileWithOplock
title: CfOpenFileWithOplock function (cfapi.h)
description: Opens an asynchronous opaque handle to a file or directory (for both normal and placeholder files) and sets up a proper oplock on it based on the open flags.
helpviewer_keywords: ["CfOpenFileWithOplock","CfOpenFileWithOplock function","cfapi/CfOpenFileWithOplock","cloudApi.cfopenfilewithoplock"]
old-location: cloudapi\cfopenfilewithoplock.htm
tech.root: cloudapi
ms.assetid: AFC48080-3B4A-4F6B-9122-25C2A025EA95
ms.date: 12/05/2018
ms.keywords: CfOpenFileWithOplock, CfOpenFileWithOplock function, cfapi/CfOpenFileWithOplock, cloudApi.cfopenfilewithoplock
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
 - CfOpenFileWithOplock
 - cfapi/CfOpenFileWithOplock
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
 - CfOpenFileWithOplock
---

# CfOpenFileWithOplock function


## -description

Opens an asynchronous opaque handle to a file or directory (for both normal and placeholder files) and sets up a proper oplock on it based on the open flags.

## -parameters

### -param FilePath [in]

Fully qualified path to the file or directory to be opened.

### -param Flags [in]

Flags to specify permissions on opening the file.

### -param ProtectedHandle [out]

An opaque handle to the file or directory that is just opened. Note that this is not a normal Win32 handle and hence cannot be used with non-CfApi Win32 APIs directly.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the oplock is broken, the API will handle the break notification automatically on behalf of the caller by draining all active requests and then closing the underneath Win32 handle.  

This aims to removing the complexity related to oplock usages. The caller must close the handle returned by <b>CfOpenFileWithOplock</b> with <a href="/windows/desktop/api/cfapi/nf-cfapi-cfclosehandle">CfCloseHandle</a>.