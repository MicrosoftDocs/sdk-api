---
UID: NF:projectedfslib.PrjFillDirEntryBuffer
title: PrjFillDirEntryBuffer function (projectedfslib.h)
description: Provides information for one file or directory to an enumeration.
helpviewer_keywords: ["PrjFillDirEntryBuffer","PrjFillDirEntryBuffer function","ProjFS.prjfilldirentrybuffer","projectedfslib/PrjFillDirEntryBuffer"]
old-location: projfs\prjfilldirentrybuffer.htm
tech.root: ProjFS
ms.assetid: CBCB0A0E-9227-42EF-B747-62783400AD16
ms.date: 12/05/2018
ms.keywords: PrjFillDirEntryBuffer, PrjFillDirEntryBuffer function, ProjFS.prjfilldirentrybuffer, projectedfslib/PrjFillDirEntryBuffer
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ProjectedFSLib.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PrjFillDirEntryBuffer
 - projectedfslib/PrjFillDirEntryBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PrjFillDirEntryBuffer
---

# PrjFillDirEntryBuffer function


## -description

Provides information for one file or directory to an enumeration.

## -parameters

### -param fileName [in]

A pointer to a null-terminated string that contains the name of the entry

### -param fileBasicInfo [in, optional]

Basic information about the entry to be filled.

### -param dirEntryBufferHandle [in]

An opaque handle to a structure that receives information about the filled entries.

## -returns

HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) indicates that dirEntryBufferHandle doesn't have enough space for the new entry.

## -remarks

The provider uses this routine to service a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback. When processing the callback, the provider calls this routine for each matching file or directory in the enumeration. 


If this routine returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) when adding an entry to the enumeration, the provider returns S_OK from the callback and waits for the next <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback. 


The provider resumes filling the enumeration with the entry it was trying to add when it got HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER). 


If this routine returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) for the first entry added during any invocation of a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback, the provider must return HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) from the callback.