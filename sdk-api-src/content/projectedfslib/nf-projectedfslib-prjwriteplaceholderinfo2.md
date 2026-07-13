---
UID: NF:projectedfslib.PrjWritePlaceholderInfo2
title: PrjWritePlaceholderInfo2 function (projectedfslib.h)
ms.date: 11/4/2019
targetos: Windows
description: Sends file or directory metadata to ProjFS and allows the caller to specify extended information.
tech.root: projfs
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
 - PrjWritePlaceholderInfo2
f1_keywords:
 - PrjWritePlaceholderInfo2
 - projectedfslib/PrjWritePlaceholderInfo2
dev_langs:
 - c++
---

# PrjWritePlaceholderInfo2 function


## -description

Sends file or directory metadata to ProjFS and allows the caller to specify extended information.

## -parameters

### -param namespaceVirtualizationContext [in]

Opaque handle for the virtualization instance. This must be the value from the VirtualizationInstanceHandle member of the callbackData passed to the provider in the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> callback.

### -param destinationFileName [in]

A null-terminated Unicode string specifying the path, relative to the virtualization root, to the file or directory for which to create a placeholder.

This must be a match to the FilePathName member of the callbackData parameter passed to the provider in the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> callback. The provider should use the PrjFileNameCompare function to determine whether the two names match.

For example, if the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> callback specifies “dir1\dir1\FILE.TXT” in callbackData-&gt;FilePathName, and the provider’s backing store contains a file called “File.txt” in the dir1\dir2 directory, and <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjfilenamecompare">PrjFileNameCompare</a> returns 0 when comparing the names “FILE.TXT” and “File.txt”, then the provider specifies “dir1\dir2\File.txt” as the value of this parameter.

### -param placeholderInfo [in]

A pointer to the metadata for the file or directory.

### -param placeholderInfoSize [in]

Size in bytes of the buffer pointed to by placeholderInfo.

### -param extendedInfo

A pointer to a <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_extended_info">PRJ_EXTENDED_INFO</a> struct specifying extended information about the placeholder to be created.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The provider uses this routine to provide the data requested in an invocation of its <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> callback, or it may use it to proactively lay down a placeholder. 

The EaInformation, SecurityInformation, and StreamsInformation members of <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info
">PRJ_PLACEHOLDER_INFO</a> are optional. If the provider does not wish to provide extended attributes, custom security descriptors, or alternate data streams, it must set these fields to 0.

### Symbolic Links

To specify that this placeholder is to be a symbolic link, the provider formats a buffer with a single <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_extended_info">PRJ_EXTENDED_INFO</a> struct and passes a pointer to it in the `extendedInfo` parameter.  The provider sets the struct's fields as follows:

* `extendedInfo.InfoType = PRJ_EXT_INFO_TYPE_SYMLINK`
* `extendedInfo.NextInfoOffset = 0`
* `extendedInfo.Symlink.TargetName = <path to the target of the symbolic link>`

## -see-also