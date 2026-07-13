---
UID: NF:projectedfslib.PrjMarkDirectoryAsPlaceholder
title: PrjMarkDirectoryAsPlaceholder function (projectedfslib.h)
description: Converts an existing directory to a directory placeholder.
helpviewer_keywords: ["PrjMarkDirectoryAsPlaceholder","PrjMarkDirectoryAsPlaceholder function","ProjFS.prjmarkdirectoryasplaceholder","projectedfslib/PrjMarkDirectoryAsPlaceholder"]
old-location: projfs\prjmarkdirectoryasplaceholder.htm
tech.root: ProjFS
ms.assetid: 6C92275E-B9A6-4556-A709-8EFBAEDB94B5
ms.date: 12/05/2018
ms.keywords: PrjMarkDirectoryAsPlaceholder, PrjMarkDirectoryAsPlaceholder function, ProjFS.prjmarkdirectoryasplaceholder, projectedfslib/PrjMarkDirectoryAsPlaceholder
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
 - PrjMarkDirectoryAsPlaceholder
 - projectedfslib/PrjMarkDirectoryAsPlaceholder
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
 - PrjMarkDirectoryAsPlaceholder
---

# PrjMarkDirectoryAsPlaceholder function


## -description

Converts an existing directory to a directory placeholder.

## -parameters

### -param rootPathName [in]

A null-terminated Unicode string specifying the full path to the virtualization root.

### -param targetPathName [in, optional]

A null-terminated Unicode string specifying the full path to the directory to convert to a placeholder.


If this parameter is not specified or is an empty string, then this means the caller wants to designate rootPathName as the virtualization root. The provider only needs to do this one time, upon establishing a new virtualization instance.

### -param versionInfo [in, optional]

Optional version information for the target placeholder. The provider chooses what information to put in the <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info">PRJ_PLACEHOLDER_VERSION_INFO</a> structure. If not specified, the placeholder gets zeros for its version information.

### -param virtualizationInstanceID [in]

A value that identifies the virtualization instance.

## -returns

HRESULT_FROM_WIN32(ERROR_REPARSE_POINT_ENCOUNTERED) typically means the directory at targetPathName has a reparse point on it. HRESULT_FROM_WIN32(ERROR_DIRECTORY) typically means the targetPathName does not specify a directory.

## -remarks

The provider must use this API to designate the virtualization root before calling <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>.