---
UID: NC:avrfsdk.AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
title: AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK (avrfsdk.h)
description: Receives information related to the enumeration of handle traces.
helpviewer_keywords: ["AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK","AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback","AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback function [Windows API]","avrfsdk/AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK","base.avrf_handleoperation_enumerate_callback","winprog.avrf_handleoperation_enumerate_callback"]
old-location: winprog\avrf_handleoperation_enumerate_callback.htm
tech.root: winprog
ms.assetid: 55949e7b-f47e-4b19-9c1d-e398db3e5ea7
ms.date: 12/05/2018
ms.keywords: AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK, AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback, AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback function [Windows API], avrfsdk/AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK, base.avrf_handleoperation_enumerate_callback, winprog.avrf_handleoperation_enumerate_callback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
 - avrfsdk/AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
---

# AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK callback function


## -description

Receives information related to the enumeration of handle traces.

## -parameters

### -param HandleOperation

A pointer to an <a href="/windows/desktop/api/avrfsdk/ns-avrfsdk-avrf_handle_operation">AVRF_HANDLE_OPERATION</a> structure containing information related to the enumeration of handle traces.

### -param EnumerationContext

A pointer to a user-defined information related to the context of the enumeration that is passed in when the <a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a> function is invoked.

### -param EnumerationLevel

A pointer to a value that informs the <a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a> function to either continue or stop the enumeration operation. These values are defined in the <a href="/windows/desktop/api/avrfsdk/ne-avrfsdk-eheapenumerationlevel">eHeapEnumerationLevel</a> enum.

## -returns

This function returns error codes or other values defined by the application.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>