---
UID: NF:projectedfslib.PrjWritePlaceholderInfo
title: PrjWritePlaceholderInfo function (projectedfslib.h)
description: Sends file or directory metadata to ProjFS.
helpviewer_keywords: ["PrjWritePlaceholderInfo","PrjWritePlaceholderInfo function","ProjFS.prjwriteplaceholderinfo","projectedfslib/PrjWritePlaceholderInfo"]
old-location: projfs\prjwriteplaceholderinfo.htm
tech.root: ProjFS
ms.assetid: EAEA2D05-2FCF-46A7-AEBD-9CF085D868E1
ms.date: 12/05/2018
ms.keywords: PrjWritePlaceholderInfo, PrjWritePlaceholderInfo function, ProjFS.prjwriteplaceholderinfo, projectedfslib/PrjWritePlaceholderInfo
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
 - PrjWritePlaceholderInfo
 - projectedfslib/PrjWritePlaceholderInfo
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
 - PrjWritePlaceholderInfo
---

# PrjWritePlaceholderInfo function


## -description

Sends file or directory metadata to ProjFS.

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

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The provider uses this routine to provide the data requested in an invocation of its <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> callback, or it may use it to proactively lay down a placeholder. 


The EaInformation, SecurityInformation, and StreamsInformation members of <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info
">PRJ_PLACEHOLDER_INFO</a> are optional. If the provider does not wish to provide extended attributes, custom security descriptors, or alternate data streams, it must set these fields to 0.