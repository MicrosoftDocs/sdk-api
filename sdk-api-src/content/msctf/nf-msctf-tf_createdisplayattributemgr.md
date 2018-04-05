---
UID: NF:msctf.TF_CreateDisplayAttributeMgr
title: TF_CreateDisplayAttributeMgr function
author: windows-driver-content
description: The TF_CreateDisplayAttributeMgr function is used to create a display attribute manager object without having to initialize COM.
old-location: tsf\tf_createdisplayattributemgr.htm
old-project: TSF
ms.assetid: d50ab73d-6266-4aaa-8053-ebbc84ec1e2c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: TF_CreateDisplayAttributeMgr, TF_CreateDisplayAttributeMgr function [Text Services Framework], msctf/TF_CreateDisplayAttributeMgr, tsf.tf_createdisplayattributemgr
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
-	TF_CreateDisplayAttributeMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# TF_CreateDisplayAttributeMgr function


## -description


The <b>TF_CreateDisplayAttributeMgr</b> function is used to create a display attribute manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that display attribute manager objects be created using <a href="_com_cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="https://msdn.microsoft.com/4a1f9a13-54a1-4294-9635-80eef8bcd8d5">ITfDisplayAttributeMgr</a>.


## -parameters




### -param ppdam [out]

Pointer to an <b>ITfDisplayAttributeMgr</b> interface pointer that receives the display attribute manager object.


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
<td><i>ppdam</i> is invalid.</td>
</tr>
</table>
 




## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/4a1f9a13-54a1-4294-9635-80eef8bcd8d5">ITfDisplayAttributeMgr
      </a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>
 

 

