---
UID: NF:msctf.TF_CreateInputProcessorProfiles
title: TF_CreateInputProcessorProfiles function
author: windows-sdk-content
description: The TF_CreateInputProcessorProfiles function is used to create a input processor profile object without having to initialize COM.
old-location: tsf\tf_createinputprocessorprofiles.htm
old-project: TSF
ms.assetid: d223736f-cf83-45a4-871e-0d6fcecb5c43
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TF_CreateInputProcessorProfiles, TF_CreateInputProcessorProfiles function [Text Services Framework], msctf/TF_CreateInputProcessorProfiles, tsf.tf_createinputprocessorprofiles
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - msctf.dll
api_name:
 - TF_CreateInputProcessorProfiles
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# TF_CreateInputProcessorProfiles function


## -description


The <b>TF_CreateInputProcessorProfiles</b> function is used to create a input processor profile object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that input processor profile objects be created using <a href="_com_cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>.


## -parameters




### -param ppipr [out]

Pointer to an <b>ITfInputProcessorProfiles</b> interface pointer that receives the input processor profile object.


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
<td><i>ppipr</i> is invalid.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles
      </a>
 

 

