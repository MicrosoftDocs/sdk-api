---
UID: NF:wsdutil.WSDFreeLinkedMemory
title: WSDFreeLinkedMemory function (wsdutil.h)
author: windows-sdk-content
description: Frees a memory block previously allocated with WSDAllocateLinkedMemory.
old-location: ncd\wsdfreelinkedmemory_func.htm
tech.root: WsdApi
ms.assetid: 8fe6f586-a262-4248-9650-dec0fae8cd74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSDFreeLinkedMemory, WSDFreeLinkedMemory function, ncd.wsdfreelinkedmemory_func, wsdutil/WSDFreeLinkedMemory
ms.topic: function
f1_keywords: 
 - "wsdutil/WSDFreeLinkedMemory"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDFreeLinkedMemory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSDFreeLinkedMemory function


## -description


Frees a memory block previously allocated with <a href="https://docs.microsoft.com/windows/desktop/api/wsdutil/nf-wsdutil-wsdallocatelinkedmemory">WSDAllocateLinkedMemory</a>.


## -parameters




### -param pVoid

Pointer to the memory block to be freed.


## -returns



This function does not return a value.




## -remarks



All children of the memory block are automatically freed.



