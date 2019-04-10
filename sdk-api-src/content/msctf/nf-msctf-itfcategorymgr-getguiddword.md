---
UID: NF:msctf.ITfCategoryMgr.GetGUIDDWORD
title: ITfCategoryMgr::GetGUIDDWORD (msctf.h)
author: windows-sdk-content
description: ITfCategoryMgr::GetGUIDDWORD method
old-location: tsf\itfcategorymgr_getguiddword.htm
tech.root: TSF
ms.assetid: 016d77b5-fc08-4d2b-a9c4-50ae7926a057
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGUIDDWORD, GetGUIDDWORD method [Text Services Framework], GetGUIDDWORD method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],GetGUIDDWORD method, ITfCategoryMgr.GetGUIDDWORD, ITfCategoryMgr::GetGUIDDWORD, _tsf_itfcategorymgr_getguiddword_ref, msctf/ITfCategoryMgr::GetGUIDDWORD, tsf.itfcategorymgr_getguiddword
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
 - msctf.dll
api_name:
 - ITfCategoryMgr.GetGUIDDWORD
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCategoryMgr::GetGUIDDWORD


## -description




## -parameters




### -param rguid [in]

Specifies the address of the GUID for which to get the value.


### -param pdw [out]

Pointer to the <b>DWORD</b> variable that receives the value of the GUID.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to get the <b>DWORD</b> value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>pdw</i> parameter was <b>NULL</b> on input.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr</a>



<a href="https://msdn.microsoft.com/674165f4-1624-46fa-b3c6-ee5242fa457b">ITfCategoryMgr::RegisterGUIDDWORD</a>



<a href="https://msdn.microsoft.com/37161b4b-7dfc-4b8d-8e0b-3b9f794eb3b0">ITfCategoryMgr::UnregisterGUIDDWORD</a>
 

 

