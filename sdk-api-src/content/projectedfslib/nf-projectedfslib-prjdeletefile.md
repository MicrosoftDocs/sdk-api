---
UID: NF:projectedfslib.PrjDeleteFile
title: PrjDeleteFile function (projectedfslib.h)
description: Enables a provider to delete an item that has been cached on the local file system.
helpviewer_keywords: ["PrjDeleteFile","PrjDeleteFile function","ProjFS.prjdeletefile","projectedfslib/PrjDeleteFile"]
old-location: projfs\prjdeletefile.htm
tech.root: ProjFS
ms.assetid: 4F3529FC-5658-4768-AC72-29178C9595F0
ms.date: 12/05/2018
ms.keywords: PrjDeleteFile, PrjDeleteFile function, ProjFS.prjdeletefile, projectedfslib/PrjDeleteFile
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
 - PrjDeleteFile
 - projectedfslib/PrjDeleteFile
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
 - PrjDeleteFile
---

# PrjDeleteFile function


## -description

Enables a provider to delete an item that has been cached on the local file system.

## -parameters

### -param namespaceVirtualizationContext [in]

An opaque handle for the virtualization instance.

### -param destinationFileName [in]

A null-terminated Unicode string specifying the path, relative to the virtualization root, to the file or directory to be deleted.

### -param updateFlags [in, optional]

Flags to control the delete operation should be allowed given the state of the file.

### -param failureReason [out, optional]

Optional pointer to receive a code describing the reason a delete failed.

## -returns

If an HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION) error is returned, the update failed due to the item's state and the value of updateFlags. failureReason, if specified, will describe the reason for the failure.

## -remarks

If the item is still in the provider's backing store, deleting it from the local file system changes it to a virtual item. 


This routine cannot be called on a virtual file/directory. 


If the file/directory to be deleted is in any state other than "placeholder", the provider must specify an appropriate combination of <a href="/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_update_types">PRJ_UPDATE_TYPES</a> values in the updateFlags parameter. This helps guard against accidental loss of data.