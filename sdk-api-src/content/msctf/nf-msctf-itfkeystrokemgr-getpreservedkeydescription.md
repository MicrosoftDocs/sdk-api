---
UID: NF:msctf.ITfKeystrokeMgr.GetPreservedKeyDescription
title: ITfKeystrokeMgr::GetPreservedKeyDescription
author: windows-sdk-content
description: ITfKeystrokeMgr::GetPreservedKeyDescription method
old-location: tsf\itfkeystrokemgr_getpreservedkeydescription.htm
tech.root: TSF
ms.assetid: 5ae2b56f-0dd9-4f37-a677-20b53c7200c7
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetPreservedKeyDescription, GetPreservedKeyDescription method [Text Services Framework], GetPreservedKeyDescription method [Text Services Framework],ITfKeystrokeMgr interface, ITfKeystrokeMgr interface [Text Services Framework],GetPreservedKeyDescription method, ITfKeystrokeMgr.GetPreservedKeyDescription, ITfKeystrokeMgr::GetPreservedKeyDescription, _tsf_itfkeystrokemgr_getpreservedkeydescription_ref, msctf/ITfKeystrokeMgr::GetPreservedKeyDescription, tsf.itfkeystrokemgr_getpreservedkeydescription
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
 - ITfKeystrokeMgr.GetPreservedKeyDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfKeystrokeMgr::GetPreservedKeyDescription


## -description




## -parameters




### -param rguid [in]

Contains the command GUID of the preserved key.


### -param pbstrDesc [out]

Pointer to a BSTR value the receives the description string. The caller must free this memory using <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters is invalid or the preserved key is not found.

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
 




## -remarks



Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.




## -see-also




<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

