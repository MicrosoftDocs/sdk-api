---
UID: NF:oleauto.SafeArrayCreate
title: SafeArrayCreate function
author: windows-sdk-content
description: Creates a new array descriptor, allocates and initializes the data for the array, and returns a pointer to the new array descriptor.
old-location: automat\safearraycreate.htm
old-project: automat
ms.assetid: 5b94f1a2-a558-473f-85dd-9545c0464cc7
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SafeArrayCreate, SafeArrayCreate function [Automation], _oa96_SafeArrayCreate, automat.safearraycreate, oleauto/SafeArrayCreate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	SafeArrayCreate
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SafeArrayCreate function


## -description


Creates a new array descriptor, allocates and initializes the data for the array, and returns a pointer to the new array descriptor.


## -parameters




### -param vt [in]

The base type of the array (the VARTYPE of each element of the array). The VARTYPE is restricted to a subset of the variant types. Neither the VT_ARRAY nor the VT_BYREF flag can be set. VT_EMPTY and VT_NULL are not valid base types for the array. All other types are legal.


### -param cDims [in]

The number of dimensions in the array. The number cannot be changed after the array is created.




### -param rgsabound [in]

A vector of bounds (one for each dimension) to allocate for the array.


## -returns



A safe array descriptor, or null if the array could not be created.



