---
UID: NF:projectedfslib.PrjStartVirtualizing
title: PrjStartVirtualizing function (projectedfslib.h)
description: Configures a ProjFS virtualization instance and starts it, making it available to service I/O and invoke callbacks on the provider.
helpviewer_keywords: ["PrjStartVirtualizing","PrjStartVirtualizing function","ProjFS.prjstartvirtualizing","projectedfslib/PrjStartVirtualizing"]
old-location: projfs\prjstartvirtualizing.htm
tech.root: ProjFS
ms.assetid: 466347B7-1D7D-4C7D-B17C-1E5E1A2223C1
ms.date: 12/05/2018
ms.keywords: PrjStartVirtualizing, PrjStartVirtualizing function, ProjFS.prjstartvirtualizing, projectedfslib/PrjStartVirtualizing
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
 - PrjStartVirtualizing
 - projectedfslib/PrjStartVirtualizing
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
 - PrjStartVirtualizing
---

# PrjStartVirtualizing function


## -description

Configures a ProjFS virtualization instance and starts it, making it available to service I/O and invoke callbacks on the provider.

## -parameters

### -param virtualizationRootPath [in]

Pointer to a null-terminated unicode string specifying the full path to the virtualization root directory.

The provider must have called <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder">PrjMarkDirectoryAsPlaceholder</a> passing the specified path as the rootPathName parameter and NULL as the targetPathName parameter before calling this routine. This only needs to be done once to designate the path as the virtualization root directory

### -param callbacks [in]

Pointer to a <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks">PRJ_CALLBACKS</a> structure that has been filled in with pointers to the provider's callback functions.

### -param instanceContext [in, optional]

Pointer to context information defined by the provider for each instance. This parameter is optional and can be NULL. If it is specified, ProjFS will return it in the InstanceContext member of <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data">PRJ_CALLBACK_DATA</a> when invoking provider callback routines.

### -param options [in, optional]

An optional pointer to a  <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_startvirtualizing_options">PRJ_STARTVIRTUALIZING_OPTIONS</a>.

### -param namespaceVirtualizationContext [out]

On success returns an opaque handle to the ProjFS virtualization instance. 
The provider passes this value when calling functions that require a PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT as input.

## -returns

The error, HRESULT_FROM_WIN32(ERROR_REPARSE_TAG_MISMATCH), indicates that virtualizationRootPath has not been configured as a virtualization root.
