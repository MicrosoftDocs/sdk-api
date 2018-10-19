---
UID: NF:msctf.TF_CreateCategoryMgr
title: TF_CreateCategoryMgr function
author: windows-sdk-content
description: The TF_CreateCategoryMgr function creates a category manager object without having to initialize COM. Usage must be done carefully because the calling thread must maintain the reference count on an object that is owned by MSCTF.DLL.
old-location: tsf\tf_createcategorymgr.htm
tech.root: TSF
ms.assetid: d157d006-c664-4086-b75e-3b90b2fa818f
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: TF_CreateCategoryMgr, TF_CreateCategoryMgr function [Text Services Framework], msctf/TF_CreateCategoryMgr, tsf.tf_createcategorymgr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - msctf.dll
api_name:
 - TF_CreateCategoryMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TF_CreateCategoryMgr function


## -description


The <b>TF_CreateCategoryMgr</b> function creates a category manager object without having to initialize COM. Usage must be done carefully because the calling thread must maintain the reference count on an object that is owned by MSCTF.DLL.


## -parameters




### -param ppcat [out]

Pointer to ITFCategoryMgr interface pointer that receives the category manager object.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>The function was successful.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 



