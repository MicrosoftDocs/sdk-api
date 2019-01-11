---
UID: NC:avrfsdk.AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
title: AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
author: windows-sdk-content
description: Receives information related to the enumeration of handle traces.
old-location: winprog\avrf_handleoperation_enumerate_callback.htm
tech.root: DevNotes
ms.assetid: 55949e7b-f47e-4b19-9c1d-e398db3e5ea7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK, AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback, AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback function [Windows API], avrfsdk/AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK, base.avrf_handleoperation_enumerate_callback, winprog.avrf_handleoperation_enumerate_callback
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
 - AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback function


## -description


Receives information related to the enumeration of handle traces.


## -parameters




### -param HandleOperation

A pointer to an <a href="https://msdn.microsoft.com/9268d24d-5000-4ac5-a3c5-895613ccbb9a">AVRF_HANDLE_OPERATION</a> structure containing information related to the enumeration of handle traces.


### -param EnumerationContext

A pointer to a user-defined information related to the context of the enumeration that is passed in when the <a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a> function is invoked.


### -param EnumerationLevel

A pointer to a value that informs the <a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a> function to either continue or stop the enumeration operation. These values are defined in the <a href="https://msdn.microsoft.com/f8260ae8-eb1e-45f4-babc-905f4af7e3b1">eHeapEnumerationLevel</a> enum.


## -returns



This function returns error codes or other values defined by the application.




## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>
 

 

