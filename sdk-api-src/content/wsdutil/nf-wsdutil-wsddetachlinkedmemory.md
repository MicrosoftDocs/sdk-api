---
UID: NF:wsdutil.WSDDetachLinkedMemory
title: WSDDetachLinkedMemory function (wsdutil.h)
description: Detaches a child memory block from its parent memory block.
helpviewer_keywords: ["WSDDetachLinkedMemory","WSDDetachLinkedMemory function","ncd.wsddetachlinkedmemory_func","wsdutil/WSDDetachLinkedMemory"]
old-location: ncd\wsddetachlinkedmemory_func.htm
tech.root: ncd
ms.assetid: a5009626-e0f8-4a04-919f-e1ae29863b05
ms.date: 12/05/2018
ms.keywords: WSDDetachLinkedMemory, WSDDetachLinkedMemory function, ncd.wsddetachlinkedmemory_func, wsdutil/WSDDetachLinkedMemory
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
 - WSDDetachLinkedMemory
 - wsdutil/WSDDetachLinkedMemory
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
 - WSDDetachLinkedMemory
---

# WSDDetachLinkedMemory function


## -description

Detaches a child memory block from its parent memory block.

## -parameters

### -param pVoid

Pointer to the memory block to be detached.

## -remarks

The child memory block must have been previously allocated by a call to <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdallocatelinkedmemory">WSDAllocateLinkedMemory</a>.