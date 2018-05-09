---
UID: NF:msctf.TF_CreateLangBarMgr
title: TF_CreateLangBarMgr function
author: windows-driver-content
description: The TF_CreateLangBarMgr function creates a language bar manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.
old-location: tsf\tf_createlangbarmgr.htm
old-project: TSF
ms.assetid: 202c5496-fc64-498e-a6f6-fffacc218990
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: TF_CreateLangBarMgr, TF_CreateLangBarMgr function [Text Services Framework], msctf/TF_CreateLangBarMgr, tsf.tf_createlangbarmgr
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	msctf.dll
api_name:
-	TF_CreateLangBarMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# TF_CreateLangBarMgr function


## -description


The <b>TF_CreateLangBarMgr</b> function creates a language bar manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that language bar manager objects be created using <a href="_com_cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="https://msdn.microsoft.com/60bd765f-0846-47f5-af1b-bc8e72720841">ITfLangBarMgr</a>.


## -parameters




### -param pppbm [out]

Pointer to an <b>ITfLangBarMgr</b> interface pointer that receives the language bar manager object.


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
<td><i>pppbm</i> is invalid.</td>
</tr>
</table>
 




## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/60bd765f-0846-47f5-af1b-bc8e72720841">ITfLangBarMgr
      </a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>
 

 

