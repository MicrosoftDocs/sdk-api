---
UID: NC:avrfsdk.AVRF_RESOURCE_ENUMERATE_CALLBACK
title: AVRF_RESOURCE_ENUMERATE_CALLBACK (avrfsdk.h)
author: windows-sdk-content
description: Provides access to one of the specialized callback functions for enumeration of either heap allocation or handle trace information.
old-location: winprog\avrf_resource_enumerate_callback.htm
tech.root: DevNotes
ms.assetid: 3f18937c-1d8f-46dd-8542-32107d358fc3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVRF_RESOURCE_ENUMERATE_CALLBACK, AVRF_RESOURCE_ENUMERATE_CALLBACK callback, AVRF_RESOURCE_ENUMERATE_CALLBACK callback function [Windows API], avrfsdk/AVRF_RESOURCE_ENUMERATE_CALLBACK, base.avrf_resource_enumerate_callback, winprog.avrf_resource_enumerate_callback
ms.topic: callback
f1_keywords: ["avrfsdk/AVRF_RESOURCE_ENUMERATE_CALLBACK"]
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
ms.custom: 19H1
---

# AVRF_RESOURCE_ENUMERATE_CALLBACK callback function


## -description


Provides access to one of the specialized callback functions for enumeration of either heap allocation or handle trace information.


## -parameters




### -param ResourceDescription

A pointer to either an <a href="https://docs.microsoft.com/windows/desktop/api/avrfsdk/ns-avrfsdk-_avrf_handle_operation">AVRF_HANDLE_OPERATION</a> structure or an <a href="https://docs.microsoft.com/windows/desktop/api/avrfsdk/ns-avrfsdk-_avrf_heap_allocation">AVRF_HEAP_ALLOCATION</a> structure. Be sure to  cast this parameter to the correct structure type.


### -param EnumerationContext

A pointer to be passed to the resource-specific callback function.


### -param EnumerationLevel

Specifies whether the enumeration operation should continue. This must be one of the values in the <a href="https://docs.microsoft.com/windows/desktop/api/avrfsdk/ne-avrfsdk-eheapenumerationlevel">eHeapEnumerationLevel</a> enum.


## -returns



This function returns error codes or other values defined by the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>
 

 

