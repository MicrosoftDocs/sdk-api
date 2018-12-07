---
UID: NF:msctf.ITfKeystrokeMgr.GetForeground
title: ITfKeystrokeMgr::GetForeground
author: windows-sdk-content
description: ITfKeystrokeMgr::GetForeground method
old-location: tsf\itfkeystrokemgr_getforeground.htm
tech.root: TSF
ms.assetid: c447c4cb-47e3-4bc7-8eba-6e102762c69b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetForeground, GetForeground method [Text Services Framework], GetForeground method [Text Services Framework],ITfKeystrokeMgr interface, ITfKeystrokeMgr interface [Text Services Framework],GetForeground method, ITfKeystrokeMgr.GetForeground, ITfKeystrokeMgr::GetForeground, _tsf_itfkeystrokemgr_getforeground_ref, msctf/ITfKeystrokeMgr::GetForeground, tsf.itfkeystrokemgr_getforeground
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeystrokeMgr.GetForeground
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfKeystrokeMgr::GetForeground


## -description




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
 



