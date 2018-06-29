---
UID: NF:bcrypt.BCryptProcessMultiOperations
title: BCryptProcessMultiOperations function
author: windows-sdk-content
description: The BCryptProcessMultiOperations function processes a sequence of operations on a multi-object state.
old-location: security\bcryptprocessmultioperation.htm
old-project: SecCNG
ms.assetid: 5FD28AC3-46D2-4F06-BF06-F5FEF8E531F5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: BCryptProcessMultiOperations, BCryptProcessMultiOperations function [Security], bcrypt/BCryptProcessMultiOperations, security.bcryptprocessmultioperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 Update [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 Update [desktop apps | UWP apps]
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
req.typenames: HASHALGORITHM_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptProcessMultiOperations
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptProcessMultiOperations function


## -description


The <b>BCryptProcessMultiOperations</b> function processes a sequence of operations on a multi-object state.


## -parameters




### -param hObject [in, out]

A handle to a multi-object state, such as one created by the <a href="https://msdn.microsoft.com/library/Mt845763(v=VS.85).aspx">BCryptCreateMultiHash</a> function.


### -param operationType [in]

A <b>BCRYPT_OPERATION_TYPE_*</b> value. Currently the only defined value is <b>BCRYPT_OPERATION_TYPE_HASH</b>. This value identifies the <i>hObject</i> parameter as a multi-hash object and the <i>pOperations</i> pointer as pointing to an array of <a href="https://msdn.microsoft.com/library/Mt845766(v=VS.85).aspx">BCRYPT_MULTI_HASH_OPERATION</a> elements.


### -param pOperations [in]

A pointer to an array of operation command structures. For hashing, it is a pointer to an array of <a href="https://msdn.microsoft.com/library/Mt845766(v=VS.85).aspx">BCRYPT_MULTI_HASH_OPERATION</a> structures.


### -param cbOperations [in]

The size, in bytes, of the <i>pOperations</i> array.


### -param dwFlags [in]

Specify a value of zero (0).


## -remarks



Each element of the <i>pOperations</i> array contains instructions for a particular computation to be performed on a single element of the multi-object state. The functional behavior of <b>BCryptProcessMultiOperations</b> is equivalent to performing, for each element in the multi-object state, the computations specified in the operations array for that element, one at a time, in order. 

The relative order of two operations that operate on different elements of the array is not guaranteed. If an output buffer overlaps an input or output buffer the result is not deterministic.




## -see-also




<a href="https://msdn.microsoft.com/library/Mt845766(v=VS.85).aspx">BCRYPT_MULTI_HASH_OPERATION</a>



<a href="https://msdn.microsoft.com/library/Mt845763(v=VS.85).aspx">BCryptCreateMultiHash</a>
 

 

