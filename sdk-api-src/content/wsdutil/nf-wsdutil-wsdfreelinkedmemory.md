---
UID: NF:wsdutil.WSDFreeLinkedMemory
title: WSDFreeLinkedMemory function (wsdutil.h)
description: Frees a memory block previously allocated with WSDAllocateLinkedMemory.
helpviewer_keywords: ["WSDFreeLinkedMemory","WSDFreeLinkedMemory function","ncd.wsdfreelinkedmemory_func","wsdutil/WSDFreeLinkedMemory"]
old-location: ncd\wsdfreelinkedmemory_func.htm
tech.root: ncd
ms.assetid: 8fe6f586-a262-4248-9650-dec0fae8cd74
ms.date: 12/05/2018
ms.keywords: WSDFreeLinkedMemory, WSDFreeLinkedMemory function, ncd.wsdfreelinkedmemory_func, wsdutil/WSDFreeLinkedMemory
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
 - WSDFreeLinkedMemory
 - wsdutil/WSDFreeLinkedMemory
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
 - WSDFreeLinkedMemory
---

# WSDFreeLinkedMemory function


## -description

Frees a memory block previously allocated with <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdallocatelinkedmemory">WSDAllocateLinkedMemory</a>.

## -parameters

### -param pVoid

Pointer to the memory block to be freed.

## -remarks

All children of the memory block are automatically freed.