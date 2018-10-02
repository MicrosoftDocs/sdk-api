---
UID: NF:msctf.ITfCategoryMgr.UnregisterGUIDDWORD
title: ITfCategoryMgr::UnregisterGUIDDWORD
author: windows-sdk-content
description: ITfCategoryMgr::UnregisterGUIDDWORD method
old-location: tsf\itfcategorymgr_unregisterguiddword.htm
tech.root: TSF
ms.assetid: 37161b4b-7dfc-4b8d-8e0b-3b9f794eb3b0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],UnregisterGUIDDWORD method, ITfCategoryMgr.UnregisterGUIDDWORD, ITfCategoryMgr::UnregisterGUIDDWORD, UnregisterGUIDDWORD, UnregisterGUIDDWORD method [Text Services Framework], UnregisterGUIDDWORD method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_unregisterguiddword_ref, msctf/ITfCategoryMgr::UnregisterGUIDDWORD, tsf.itfcategorymgr_unregisterguiddword
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
 - msctf.dll
api_name:
 - ITfCategoryMgr.UnregisterGUIDDWORD
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCategoryMgr::UnregisterGUIDDWORD


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the GUID.


### -param rguid [in]

Contains the GUID that the <b>DWORD</b> is removed for.


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
The GUID cannot be found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/016d77b5-fc08-4d2b-a9c4-50ae7926a057">ITfCategoryMgr::GetGUIDDWORD
      </a>



<a href="https://msdn.microsoft.com/674165f4-1624-46fa-b3c6-ee5242fa457b">ITfCategoryMgr::RegisterGUIDDWORD
      </a>
 

 

