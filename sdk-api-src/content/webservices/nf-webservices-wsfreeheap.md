---
UID: NF:webservices.WsFreeHeap
title: WsFreeHeap function
author: windows-sdk-content
description: This frees the heap object, and the memory associated with any allocations made on it using WsAlloc.
old-location: wsw\wsfreeheap.htm
tech.root: wsw
ms.assetid: ec643915-8c4b-4916-b390-d6ca043350db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsFreeHeap, WsFreeHeap function [Web Services for Windows], webservices/WsFreeHeap, wsw.wsfreeheap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFreeHeap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsFreeHeap function


## -description


This frees the heap object, and the memory associated with any allocations 
                made on it using <a href="https://msdn.microsoft.com/633b6a11-09ba-48a7-a1ad-940846c65d79">WsAlloc</a>.
            


## -parameters




### -param heap [in]

The heap to free.  This must be a valid heap object that was returned
                    from <a href="https://msdn.microsoft.com/459b7146-3b32-4df8-87e1-4ac7ad33ed0e">WsCreateHeap</a>.  This parameter may not be <b>NULL</b>.
                


## -returns



This function does not return a value.



