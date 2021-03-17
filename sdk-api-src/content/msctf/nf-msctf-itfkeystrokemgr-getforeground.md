---
UID: NF:msctf.ITfKeystrokeMgr.GetForeground
title: ITfKeystrokeMgr::GetForeground (msctf.h)
description: ITfKeystrokeMgr::GetForeground method
helpviewer_keywords: ["GetForeground","GetForeground method [Text Services Framework]","GetForeground method [Text Services Framework]","ITfKeystrokeMgr interface","ITfKeystrokeMgr interface [Text Services Framework]","GetForeground method","ITfKeystrokeMgr.GetForeground","ITfKeystrokeMgr::GetForeground","_tsf_itfkeystrokemgr_getforeground_ref","msctf/ITfKeystrokeMgr::GetForeground","tsf.itfkeystrokemgr_getforeground"]
old-location: tsf\itfkeystrokemgr_getforeground.htm
tech.root: TSF
ms.assetid: c447c4cb-47e3-4bc7-8eba-6e102762c69b
ms.date: 12/05/2018
ms.keywords: GetForeground, GetForeground method [Text Services Framework], GetForeground method [Text Services Framework],ITfKeystrokeMgr interface, ITfKeystrokeMgr interface [Text Services Framework],GetForeground method, ITfKeystrokeMgr.GetForeground, ITfKeystrokeMgr::GetForeground, _tsf_itfkeystrokemgr_getforeground_ref, msctf/ITfKeystrokeMgr::GetForeground, tsf.itfkeystrokemgr_getforeground
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfKeystrokeMgr::GetForeground
 - msctf/ITfKeystrokeMgr::GetForeground
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeystrokeMgr.GetForeground
---

# ITfKeystrokeMgr::GetForeground


## -description

Obtains the class identifier of the foreground TSF text service.

## -parameters

### -param pclsid [out]

Pointer to a CLSID that receives the class identifier of the foreground TSF text service.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no foreground text service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pclsid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

