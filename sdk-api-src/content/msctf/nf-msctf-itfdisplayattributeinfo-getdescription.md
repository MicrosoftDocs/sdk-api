---
UID: NF:msctf.ITfDisplayAttributeInfo.GetDescription
title: ITfDisplayAttributeInfo::GetDescription
author: windows-sdk-content
description: ITfDisplayAttributeInfo::GetDescription method
old-location: tsf\itfdisplayattributeinfo_getdescription.htm
tech.root: TSF
ms.assetid: e65aedac-284d-4e2a-b574-fc469f66e06e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDescription, GetDescription method [Text Services Framework], GetDescription method [Text Services Framework],ITfDisplayAttributeInfo interface, ITfDisplayAttributeInfo interface [Text Services Framework],GetDescription method, ITfDisplayAttributeInfo.GetDescription, ITfDisplayAttributeInfo::GetDescription, _tsf_itfdisplayattributeinfo_getdescription_ref, msctf/ITfDisplayAttributeInfo::GetDescription, tsf.itfdisplayattributeinfo_getdescription
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
 - ITfDisplayAttributeInfo.GetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfDisplayAttributeInfo::GetDescription


## -description




## -parameters




### -param pbstrDesc [out]

Pointer to a BSTR value that receives the description string. This value must be allocated using <a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The caller must free this memory using <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


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
<i>pbstrDesc</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a>



<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

