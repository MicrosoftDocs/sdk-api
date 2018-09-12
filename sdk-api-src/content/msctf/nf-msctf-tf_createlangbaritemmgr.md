---
UID: NF:msctf.TF_CreateLangBarItemMgr
title: TF_CreateLangBarItemMgr function
author: windows-sdk-content
description: The TF_CreateLangBarItemMgr function is used to create a language bar item manager object without having to initialize COM.
old-location: tsf\tf_createlangbaritemmgr.htm
tech.root: TSF
ms.assetid: b7492732-ae06-4344-b5c0-97b3734af36a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TF_CreateLangBarItemMgr, TF_CreateLangBarItemMgr function [Text Services Framework], msctf/TF_CreateLangBarItemMgr, tsf.tf_createlangbaritemmgr
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
 - TF_CreateLangBarItemMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TF_CreateLangBarItemMgr function


## -description


The <b>TF_CreateLangBarItemMgr</b> function is used to create a language bar item manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that language bar item manager objects be created using <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> , as demonstrated in <a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr
      </a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>
 

 

