---
UID: NF:projectedfslib.PrjGetOnDiskFileState
title: PrjGetOnDiskFileState function (projectedfslib.h)
description: Gets the on-disk file state for a file or directory.
helpviewer_keywords: ["PrjGetOnDiskFileState","PrjGetOnDiskFileState function","ProjFS.prjgetondiskfilestate","projectedfslib/PrjGetOnDiskFileState"]
old-location: projfs\prjgetondiskfilestate.htm
tech.root: ProjFS
ms.assetid: E302C472-1360-43D9-8AB9-26C93F97F00F
ms.date: 12/05/2018
ms.keywords: PrjGetOnDiskFileState, PrjGetOnDiskFileState function, ProjFS.prjgetondiskfilestate, projectedfslib/PrjGetOnDiskFileState
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
 - PrjGetOnDiskFileState
 - projectedfslib/PrjGetOnDiskFileState
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
 - PrjGetOnDiskFileState
---

# PrjGetOnDiskFileState function


## -description

Gets the on-disk file state for a file or directory.

## -parameters

### -param destinationFileName [in]

A null-terminated Unicode string specifying the full path to the file whose state is to be queried.

### -param fileState [out]

This is a combination of one or more PRJ_FILE_STATE values describing the file state.

## -returns

HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) indicates destinationFileName does not exist. HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) indicates that an intermediate component of the path to destinationFileName does not exist.

## -remarks

This routine tells the caller what the ProjFS caching state is of the specified file or directory. For example, the caller can use this routine to determine whether the given item is a placeholder or full file. 


A running provider should be cautious if using this routine on files or directories within one of its virtualization instances, as it may cause callbacks to be invoked in the provider. Depending on the design of the provider this may lead to deadlocks.

