---
UID: NF:wsdutil.WSDAllocateLinkedMemory
title: WSDAllocateLinkedMemory function (wsdutil.h)
description: Allocates a linked memory block.
helpviewer_keywords: ["WSDAllocateLinkedMemory","WSDAllocateLinkedMemory function","ncd.wsdallocatelinkedmemory_func","wsdutil/WSDAllocateLinkedMemory"]
old-location: ncd\wsdallocatelinkedmemory_func.htm
tech.root: ncd
ms.assetid: 2608985f-56aa-4223-b76d-85ebe3b080fb
ms.date: 12/05/2018
ms.keywords: WSDAllocateLinkedMemory, WSDAllocateLinkedMemory function, ncd.wsdallocatelinkedmemory_func, wsdutil/WSDAllocateLinkedMemory
req.header: wsdutil.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDAllocateLinkedMemory
 - wsdutil/WSDAllocateLinkedMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDAllocateLinkedMemory
---

# WSDAllocateLinkedMemory function


## -description

Allocates a linked memory block.

## -parameters

### -param pParent

 Pointer to the parent memory block.

### -param cbSize

Size of the memory block to be allocated.

## -returns

Pointer to the newly allocated memory block.

## -remarks

The memory 
block allocated by <b>WSDAllocateLinkedMemory</b> is linked to a parent memory block and is freed when 
the parent memory block is freed.

 If <i>pParent</i> is <b>NULL</b> the allocated memory block must be explicitly freed by calling 
<a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a>.