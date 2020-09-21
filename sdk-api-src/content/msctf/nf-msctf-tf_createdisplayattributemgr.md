---
UID: NF:msctf.TF_CreateDisplayAttributeMgr
title: TF_CreateDisplayAttributeMgr function (msctf.h)
description: The TF_CreateDisplayAttributeMgr function is used to create a display attribute manager object without having to initialize COM.
helpviewer_keywords: ["TF_CreateDisplayAttributeMgr","TF_CreateDisplayAttributeMgr function [Text Services Framework]","msctf/TF_CreateDisplayAttributeMgr","tsf.tf_createdisplayattributemgr"]
old-location: tsf\tf_createdisplayattributemgr.htm
tech.root: TSF
ms.assetid: d50ab73d-6266-4aaa-8053-ebbc84ec1e2c
ms.date: 12/05/2018
ms.keywords: TF_CreateDisplayAttributeMgr, TF_CreateDisplayAttributeMgr function [Text Services Framework], msctf/TF_CreateDisplayAttributeMgr, tsf.tf_createdisplayattributemgr
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
 - TF_CreateDisplayAttributeMgr
 - msctf/TF_CreateDisplayAttributeMgr
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
 - TF_CreateDisplayAttributeMgr
---

# TF_CreateDisplayAttributeMgr function


## -description

The <b>TF_CreateDisplayAttributeMgr</b> function is used to create a display attribute manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that display attribute manager objects be created using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributemgr">ITfDisplayAttributeMgr</a>.

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

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributemgr">ITfDisplayAttributeMgr
      </a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>