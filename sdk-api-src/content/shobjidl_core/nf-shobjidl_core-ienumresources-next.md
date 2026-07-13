---
UID: NF:shobjidl_core.IEnumResources.Next
title: IEnumResources::Next (shobjidl_core.h)
description: Gets the next SHELL_ITEM_RESOURCE structure.
helpviewer_keywords: ["IEnumResources interface [Windows Shell]","Next method","IEnumResources.Next","IEnumResources::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumResources interface","_shell_IEnumResources_Next","shell.IEnumResources_Next","shobjidl_core/IEnumResources::Next"]
old-location: shell\IEnumResources_Next.htm
tech.root: shell
ms.assetid: b5d0d754-4252-476a-b3af-0ba257eab339
ms.date: 12/05/2018
ms.keywords: IEnumResources interface [Windows Shell],Next method, IEnumResources.Next, IEnumResources::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumResources interface, _shell_IEnumResources_Next, shell.IEnumResources_Next, shobjidl_core/IEnumResources::Next
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumResources::Next
 - shobjidl_core/IEnumResources::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumResources.Next
---

# IEnumResources::Next


## -description

Gets the next <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a> structure.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of resources requested. Currently, must be 1.

### -param psir [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a>*</b>

Receives a pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a> structure.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of resources retrieved. Currently, not used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.