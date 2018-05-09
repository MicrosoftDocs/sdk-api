---
UID: NF:msctf.ITfFunction.GetDisplayName
title: ITfFunction::GetDisplayName
author: windows-driver-content
description: ITfFunction::GetDisplayName method
old-location: tsf\itffunction_getdisplayname.htm
old-project: TSF
ms.assetid: da52ca6d-9606-45c5-8db9-c876c827df14
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetDisplayName, GetDisplayName method [Text Services Framework], GetDisplayName method [Text Services Framework],ITfFunction interface, ITfFunction interface [Text Services Framework],GetDisplayName method, ITfFunction.GetDisplayName, ITfFunction::GetDisplayName, _tsf_itffunction_getdisplayname_ref, msctf/ITfFunction::GetDisplayName, tsf.itffunction_getdisplayname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfFunction.GetDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfFunction::GetDisplayName


## -description




## -parameters




### -param pbstrName [out]

Pointer to a BSTR value that receives the display name. This value must be allocated using <a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The caller must free this memory using <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbstrName</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/140b1ed8-8876-4f06-8ed2-7b0dccdc0a69">ITfFunction</a>



<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

