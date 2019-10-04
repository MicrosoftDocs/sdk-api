---
UID: NF:shlwapi.IStream_WritePidl
title: IStream_WritePidl function (shlwapi.h)
author: windows-sdk-content
description: Writes a pointer to an item identifier list (PIDL) from a PCUIDLIST_RELATIVE object into an IStream object.
old-location: shell\IStream_WritePidl.htm
tech.root: shell
ms.assetid: 29b6a42b-08bd-4b5f-92ad-a6456e7a6f98
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStream_WritePidl, IStream_WritePidl function [Windows Shell], _shell_IStream_WritePidl, shell.IStream_WritePidl, shlwapi/IStream_WritePidl
ms.topic: function
f1_keywords: 
 - "shlwapi/IStream_WritePidl"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - IStream_WritePidl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStream_WritePidl function


## -description


Writes a pointer to an item identifier list (PIDL) from a PCUIDLIST_RELATIVE object into an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object.


## -parameters




### -param pstm [in]

Type: <b>IStream*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object in which to write.


### -param pidlWrite [in]

Type: <b>PCUIDLIST_RELATIVE</b>

The source PIDL.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



