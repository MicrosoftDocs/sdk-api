---
UID: NF:msctf.TF_CreateInputProcessorProfiles
title: TF_CreateInputProcessorProfiles function (msctf.h)
description: The TF_CreateInputProcessorProfiles function is used to create a input processor profile object without having to initialize COM.
helpviewer_keywords: ["TF_CreateInputProcessorProfiles","TF_CreateInputProcessorProfiles function [Text Services Framework]","msctf/TF_CreateInputProcessorProfiles","tsf.tf_createinputprocessorprofiles"]
old-location: tsf\tf_createinputprocessorprofiles.htm
tech.root: TSF
ms.assetid: d223736f-cf83-45a4-871e-0d6fcecb5c43
ms.date: 12/05/2018
ms.keywords: TF_CreateInputProcessorProfiles, TF_CreateInputProcessorProfiles function [Text Services Framework], msctf/TF_CreateInputProcessorProfiles, tsf.tf_createinputprocessorprofiles
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_CreateInputProcessorProfiles
 - msctf/TF_CreateInputProcessorProfiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - msctf.dll
api_name:
 - TF_CreateInputProcessorProfiles
---

# TF_CreateInputProcessorProfiles function


## -description

The <b>TF_CreateInputProcessorProfiles</b> function is used to create a input processor profile object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that input processor profile objects be created using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>.

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

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles
      </a>