---
UID: NF:shlwapi.IStream_ReadPidl
title: IStream_ReadPidl function (shlwapi.h)
description: Reads a pointer to an item identifier list (PIDL) from an IStream object into a PIDLIST_RELATIVE object.
helpviewer_keywords: ["IStream_ReadPidl","IStream_ReadPidl function [Windows Shell]","_shell_IStream_ReadPidl","shell.IStream_ReadPidl","shlwapi/IStream_ReadPidl"]
old-location: shell\IStream_ReadPidl.htm
tech.root: shell
ms.assetid: 63b1f842-139b-4558-8105-4986ce592b56
ms.date: 12/05/2018
ms.keywords: IStream_ReadPidl, IStream_ReadPidl function [Windows Shell], _shell_IStream_ReadPidl, shell.IStream_ReadPidl, shlwapi/IStream_ReadPidl
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStream_ReadPidl
 - shlwapi/IStream_ReadPidl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - IStream_ReadPidl
---

# IStream_ReadPidl function


## -description

Reads a pointer to an item identifier list (PIDL) from an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object into a PIDLIST_RELATIVE object.

## -parameters

### -param pstm [in]

Type: <b>IStream*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> from which the PIDL is read.

### -param ppidlOut [out]

Type: <b>PIDLIST_RELATIVE*</b>

A pointer to the resulting PIDL.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.