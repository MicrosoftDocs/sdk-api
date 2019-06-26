---
UID: NF:msctf.TF_CreateThreadMgr
title: TF_CreateThreadMgr function (msctf.h)
author: windows-sdk-content
description: The TF_CreateThreadMgr function creates a thread manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.
old-location: tsf\tf_createthreadmgr.htm
tech.root: TSF
ms.assetid: 470cc721-598e-480d-a41c-354704b4d058
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TF_CreateThreadMgr, TF_CreateThreadMgr function [Text Services Framework], msctf/TF_CreateThreadMgr, tsf.tf_createthreadmgr
ms.topic: function
f1_keywords: 
 - "msctf/TF_CreateThreadMgr"
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
ms.custom: 19H1
---

# TF_CreateThreadMgr function


## -description


The <b>TF_CreateThreadMgr</b> function creates a thread manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that thread manager objects be created using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>
 

 

