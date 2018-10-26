---
UID: NC:avrfsdk.AVRF_RESOURCE_ENUMERATE_CALLBACK
title: AVRF_RESOURCE_ENUMERATE_CALLBACK
author: windows-sdk-content
description: Provides access to one of the specialized callback functions for enumeration of either heap allocation or handle trace information.
old-location: winprog\avrf_resource_enumerate_callback.htm
tech.root: devnotes
ms.assetid: 3f18937c-1d8f-46dd-8542-32107d358fc3
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: AVRF_RESOURCE_ENUMERATE_CALLBACK, AVRF_RESOURCE_ENUMERATE_CALLBACK callback, AVRF_RESOURCE_ENUMERATE_CALLBACK callback function [Windows API], avrfsdk/AVRF_RESOURCE_ENUMERATE_CALLBACK, base.avrf_resource_enumerate_callback, winprog.avrf_resource_enumerate_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: avrfsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_RESOURCE_ENUMERATE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVRF_RESOURCE_ENUMERATE_CALLBACK callback function


## -description


Provides access to one of the specialized callback functions for enumeration of either heap allocation or handle trace information.


## -parameters




### -param ResourceDescription

A pointer to either an <a href="https://msdn.microsoft.com/9268d24d-5000-4ac5-a3c5-895613ccbb9a">AVRF_HANDLE_OPERATION</a> structure or an <a href="https://msdn.microsoft.com/238c7de7-4bf1-4974-8a6f-09e4d5f756ab">AVRF_HEAP_ALLOCATION</a> structure. Be sure to  cast this parameter to the correct structure type.


### -param EnumerationContext

A pointer to be passed to the resource-specific callback function.


### -param EnumerationLevel

Specifies whether the enumeration operation should continue. This must be one of the values in the <a href="https://msdn.microsoft.com/f8260ae8-eb1e-45f4-babc-905f4af7e3b1">eHeapEnumerationLevel</a> enum.


## -returns



This function returns error codes or other values defined by the application.




## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

