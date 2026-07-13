---
UID: NF:projectedfslib.PrjFillDirEntryBuffer2
title: PrjFillDirEntryBuffer2 function (projectedfslib.h)
description: Provides information for one file or directory to an enumeration and allows the caller to specify extended information.
tech.root: projfs
ms.date: 11/4/2019
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: projectedfslib.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: ProjectedFSLib.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 20H1
topic_type:
 - apiref
api_type:
api_location:
 - projectedfslib.h
api_name:
 - PrjFillDirEntryBuffer2
f1_keywords:
 - PrjFillDirEntryBuffer2
 - projectedfslib/PrjFillDirEntryBuffer2
dev_langs:
 - c++
---

# PrjFillDirEntryBuffer2 function


## -description

Provides information for one file or directory to an enumeration and allows the caller to specify extended information.

## -parameters

### -param dirEntryBufferHandle [in]

An opaque handle to a structure that receives information about the filled entries.

### -param fileName [in]

A pointer to a null-terminated string that contains the name of the entry

### -param fileBasicInfo [in, optional]

Basic information about the entry to be filled.

### -param extendedInfo [in, optional]

A pointer to a <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_extended_info">PRJ_EXTENDED_INFO</a> struct specifying extended information about the entry to be filled.

## -returns

HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) indicates that dirEntryBufferHandle doesn't have enough space for the new entry.

E_INVALIDARG indicates that extendedInfo.InfoType is unrecognized.

## -remarks

The provider uses this routine to service a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback. When processing the callback, the provider calls this routine for each matching file or directory in the enumeration. This routine allows the provider to specify extended information about the file or directory, such as whether it is a symbolic link.

If this routine returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) when adding an entry to the enumeration, the provider returns S_OK from the callback and waits for the next <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback.

The provider resumes filling the enumeration with the entry it was trying to add when it got HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).

If this routine returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) for the first entry added during any invocation of a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback, the provider must return HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) from the callback.

### Symbolic Links

To specify that this directory entry is for a symbolic link, the provider formats a buffer with a single <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_extended_info">PRJ_EXTENDED_INFO</a> struct and passes a pointer to it in the `extendedInfo` parameter.  The provider sets the struct's fields as follows:

* `extendedInfo.InfoType = PRJ_EXT_INFO_TYPE_SYMLINK`
* `extendedInfo.NextInfoOffset = 0`
* `extendedInfo.Symlink.TargetName = <path to the target of the symbolic link>`

## -see-also