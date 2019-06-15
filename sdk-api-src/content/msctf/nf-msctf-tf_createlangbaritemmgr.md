---
UID: NF:msctf.TF_CreateLangBarItemMgr
title: TF_CreateLangBarItemMgr function (msctf.h)
author: windows-sdk-content
description: The TF_CreateLangBarItemMgr function is used to create a language bar item manager object without having to initialize COM.
old-location: tsf\tf_createlangbaritemmgr.htm
tech.root: TSF
ms.assetid: b7492732-ae06-4344-b5c0-97b3734af36a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TF_CreateLangBarItemMgr, TF_CreateLangBarItemMgr function [Text Services Framework], msctf/TF_CreateLangBarItemMgr, tsf.tf_createlangbaritemmgr
ms.topic: function
f1_keywords: ["msctf/TF_CreateLangBarItemMgr"]
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
 - TF_CreateLangBarItemMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# TF_CreateLangBarItemMgr function


## -description


The <b>TF_CreateLangBarItemMgr</b> function is used to create a language bar item manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that language bar item manager objects be created using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>.


## -parameters




### -param pplbim [out]

Pointer to an <b>ITfLangBarItemMgr</b> interface pointer that receives the language bar item manager object.


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
<td><i>pplbim</i> is invalid.</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>
 

 

