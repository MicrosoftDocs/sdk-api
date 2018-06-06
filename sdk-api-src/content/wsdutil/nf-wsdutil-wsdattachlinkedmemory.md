---
UID: NF:wsdutil.WSDAttachLinkedMemory
title: WSDAttachLinkedMemory function
author: windows-sdk-content
description: Attaches a child memory block to a parent memory block.
old-location: ncd\wsdattachlinkedmemory_func.htm
old-project: WsdApi
ms.assetid: 4f7bc268-6fcf-42f2-8457-e5094bee6e68
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSDAttachLinkedMemory, WSDAttachLinkedMemory function, ncd.wsdattachlinkedmemory_func, wsdutil/WSDAttachLinkedMemory
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
 - WSDAttachLinkedMemory
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDAttachLinkedMemory function


## -description


Attaches a child memory block to a
parent memory block. Multiple children can be attached to a parent memory block.


## -parameters




### -param pParent

Pointer to the parent memory block.


### -param pChild

Pointer to the child memory block.


## -returns



This function does not return a value.




## -remarks



The child memory block is automatically freed when the parent memory
block is freed. Both the parent and child memory blocks must have been previously allocated by calls to <a href="https://msdn.microsoft.com/2608985f-56aa-4223-b76d-85ebe3b080fb">WSDAllocateLinkedMemory</a>.



