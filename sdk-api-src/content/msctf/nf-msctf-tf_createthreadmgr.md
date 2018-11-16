---
UID: NF:msctf.TF_CreateThreadMgr
title: TF_CreateThreadMgr function
author: windows-sdk-content
description: The TF_CreateThreadMgr function creates a thread manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.
old-location: tsf\tf_createthreadmgr.htm
tech.root: TSF
ms.assetid: 470cc721-598e-480d-a41c-354704b4d058
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TF_CreateThreadMgr, TF_CreateThreadMgr function [Text Services Framework], msctf/TF_CreateThreadMgr, tsf.tf_createthreadmgr
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
 - TF_CreateThreadMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- 
: 
- TF_CreateThreadMgr
: 
---

# TF_CreateThreadMgr function


## -description


The <b>TF_CreateThreadMgr</b> function creates a thread manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that thread manager objects be created using <a href="_com_cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>.


## -parameters




### -param pptim [out]

Pointer to an <b>ITfThreadMgr</b> interface pointer that receives the thread manager object.


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
<tr>
<td>E_INVALIDARG</td>
<td><i>pptim</i> is invalid.</td>
</tr>
</table>
 




## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
      </a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>
 

 

