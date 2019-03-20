---
UID: NF:combaseapi.FreePropVariantArray
title: FreePropVariantArray function (combaseapi.h)
author: windows-sdk-content
description: The FreePropVariantArray function calls PropVariantClear on each of the PROPVARIANT structures in the rgvars array to make the value zero for each of the members of the array.
old-location: stg\freepropvariantarray.htm
tech.root: Stg
ms.assetid: 2eefb57e-9311-46e1-9eed-e25aa3b5afaa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FreePropVariantArray, FreePropVariantArray function [Structured Storage], _stg_freepropvariantarray, combaseapi/FreePropVariantArray, stg.freepropvariantarray
ms.topic: function
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - FreePropVariantArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreePropVariantArray function


## -description


The <b>FreePropVariantArray</b> function calls 
<a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a> on each of the 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures in the <i>rgvars</i> array to make the value zero for each of the members of the array.


## -parameters




### -param cVariants [in]

Count of elements in the 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> array (<i>rgvars</i>).


### -param rgvars [in]

Pointer to an initialized array of 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures for which any deallocatable elements are to be freed. On exit, all zeroes are written to the 
<b>PROPVARIANT</b> structure (thus tagging them as VT_EMPTY).


## -returns



This function returns HRESULT.




## -remarks



<b>FreePropVariantArray</b> calls 
<a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a> on an array of 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures to clear all the valid members. All valid 
<b>PROPVARIANT</b> structures are freed. If any of the 
<b>PROPVARIANT</b> structures contain illegal VT types, valid members are freed and the function returns STG_E_INVALIDPARAMETER.

Passing <b>NULL</b> for <i>rgvars</i> is legal, and produces a return code of S_OK.




## -see-also




<a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a>
 

 

