---
UID: NF:msctf.TF_CreateLangBarMgr
title: TF_CreateLangBarMgr function (msctf.h)
description: The TF_CreateLangBarMgr function creates a language bar manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.
helpviewer_keywords: ["TF_CreateLangBarMgr","TF_CreateLangBarMgr function [Text Services Framework]","msctf/TF_CreateLangBarMgr","tsf.tf_createlangbarmgr"]
old-location: tsf\tf_createlangbarmgr.htm
tech.root: TSF
ms.assetid: 202c5496-fc64-498e-a6f6-fffacc218990
ms.date: 12/05/2018
ms.keywords: TF_CreateLangBarMgr, TF_CreateLangBarMgr function [Text Services Framework], msctf/TF_CreateLangBarMgr, tsf.tf_createlangbarmgr
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
 - TF_CreateLangBarMgr
 - msctf/TF_CreateLangBarMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-tsf-msctf-l1-1-4.dll
 - ext-ms-win-tsf-msctf-l1-1-3.dll
 - ext-ms-win-tsf-msctf-l1-1-2.dll
 - msctf.dll
api_name:
 - TF_CreateLangBarMgr
---

# TF_CreateLangBarMgr function


## -description

The <b>TF_CreateLangBarMgr</b> function creates a language bar manager object without having to initialize COM. Usage of this method is not recommended, because the calling process must maintain a proper reference count on an object that is owned by Msctf.dll.

It is instead recommended that language bar manager objects be created using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> , as demonstrated in <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbarmgr">ITfLangBarMgr</a>.

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

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbarmgr">ITfLangBarMgr
      </a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>