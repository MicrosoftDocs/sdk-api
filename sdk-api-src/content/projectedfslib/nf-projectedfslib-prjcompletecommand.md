---
UID: NF:projectedfslib.PrjCompleteCommand
title: PrjCompleteCommand function (projectedfslib.h)
description: Indicates that the provider has completed processing a callback from which it had previously returned HRESULT_FROM_WIN32(ERROR_IO_PENDING).
helpviewer_keywords: ["PrjCompleteCommand","PrjCompleteCommand function","ProjFS.prjcompletecommand","projectedfslib/PrjCompleteCommand"]
old-location: projfs\prjcompletecommand.htm
tech.root: ProjFS
ms.assetid: 9A47FAB5-A085-41C9-861C-E74F2F5AF474
ms.date: 12/05/2018
ms.keywords: PrjCompleteCommand, PrjCompleteCommand function, ProjFS.prjcompletecommand, projectedfslib/PrjCompleteCommand
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
 - PrjCompleteCommand
 - projectedfslib/PrjCompleteCommand
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
 - PrjCompleteCommand
---

# PrjCompleteCommand function


## -description

Indicates that the provider has completed processing a callback from which it had previously returned HRESULT_FROM_WIN32(ERROR_IO_PENDING).

## -parameters

### -param namespaceVirtualizationContext [in]

Opaque handle for the virtualization instance. This must be the value from the VirtualizationInstanceHandle member of the callbackData passed to the provider in the callback that is being complete.

### -param commandId [in]

A value identifying the callback invocation that the provider is completing. This must be the value from the CommandId member of the callbackData passed to the provider in the callback that is being completed.

### -param completionResult [in]

The final HRESULT of the operation.

### -param extendedParameters [in, optional]

Optional pointer to extended parameters required for completing certain callbacks.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

