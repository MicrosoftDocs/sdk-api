---
UID: NF:wsdutil.WSDAllocateLinkedMemory
title: WSDAllocateLinkedMemory function
author: windows-sdk-content
description: Allocates a linked memory block.
old-location: ncd\wsdallocatelinkedmemory_func.htm
old-project: WsdApi
ms.assetid: 2608985f-56aa-4223-b76d-85ebe3b080fb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WSDAllocateLinkedMemory, WSDAllocateLinkedMemory function, ncd.wsdallocatelinkedmemory_func, wsdutil/WSDAllocateLinkedMemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RESPONSEBODY_SubscriptionEnd
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDAllocateLinkedMemory
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.



