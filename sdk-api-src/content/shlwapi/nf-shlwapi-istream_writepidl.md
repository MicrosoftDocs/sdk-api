---
UID: NF:shlwapi.IStream_WritePidl
title: IStream_WritePidl function (shlwapi.h)
description: Writes a pointer to an item identifier list (PIDL) from a PCUIDLIST_RELATIVE object into an IStream object.
helpviewer_keywords: ["IStream_WritePidl","IStream_WritePidl function [Windows Shell]","_shell_IStream_WritePidl","shell.IStream_WritePidl","shlwapi/IStream_WritePidl"]
old-location: shell\IStream_WritePidl.htm
tech.root: shell
ms.assetid: 29b6a42b-08bd-4b5f-92ad-a6456e7a6f98
ms.date: 12/05/2018
ms.keywords: IStream_WritePidl, IStream_WritePidl function [Windows Shell], _shell_IStream_WritePidl, shell.IStream_WritePidl, shlwapi/IStream_WritePidl
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
 - IStream_WritePidl
 - shlwapi/IStream_WritePidl
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
 - IStream_WritePidl
---

# IStream_WritePidl function


## -description

Writes a pointer to an item identifier list (PIDL) from a PCUIDLIST_RELATIVE object into an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object.

## -parameters

### -param pstm [in]

Type: <b>IStream*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object in which to write.

### -param pidlWrite [in]

Type: <b>PCUIDLIST_RELATIVE</b>

The source PIDL.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.