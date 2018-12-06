---
UID: NF:wsdutil.WSDDetachLinkedMemory
title: WSDDetachLinkedMemory function
author: windows-sdk-content
description: Detaches a child memory block from its parent memory block.
old-location: ncd\wsddetachlinkedmemory_func.htm
tech.root: wsdapi
ms.assetid: a5009626-e0f8-4a04-919f-e1ae29863b05
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSDDetachLinkedMemory, WSDDetachLinkedMemory function, ncd.wsddetachlinkedmemory_func, wsdutil/WSDDetachLinkedMemory
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WSDDetachLinkedMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSDDetachLinkedMemory function


## -description


Detaches a child memory block from its parent memory block.


## -parameters




### -param pVoid

Pointer to the memory block to be detached.


## -returns



This function does not return a value.




## -remarks



The child memory block must have been previously allocated by a call to <a href="https://msdn.microsoft.com/2608985f-56aa-4223-b76d-85ebe3b080fb">WSDAllocateLinkedMemory</a>.



