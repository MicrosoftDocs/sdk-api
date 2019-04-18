---
UID: NF:oleauto.SafeArrayCreateVector
title: SafeArrayCreateVector function (oleauto.h)
author: windows-sdk-content
description: Creates a one-dimensional array. A safe array created with SafeArrayCreateVector is a fixed size, so the constant FADF_FIXEDSIZE is always set.
old-location: automat\safearraycreatevector.htm
tech.root: automat
ms.assetid: b794b8c6-a523-4636-8681-a936dff3fc6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SafeArrayCreateVector, SafeArrayCreateVector function [Automation], _oa96_SafeArrayCreateVector, automat.safearraycreatevector, oleauto/SafeArrayCreateVector
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayCreateVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SafeArrayCreateVector function


## -description


Creates a one-dimensional array. A safe array created with <b>SafeArrayCreateVector</b> is a fixed size, so the constant FADF_FIXEDSIZE is always set.


## -parameters




### -param vt [in]

The base type of the array (the VARTYPE of each element of the array). The VARTYPE is restricted to a subset of the variant types. Neither the VT_ARRAY nor the VT_BYREF flag can be set. VT_EMPTY and VT_NULL are not valid base types for the array. All other types are legal.


### -param lLbound [in]

The lower bound for the array. This parameter can be negative.


### -param cElements [in]

The number of elements in the array.


## -returns



A safe array descriptor, or null if the array could not be created.




## -see-also




<a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>



<a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a>
 

 

