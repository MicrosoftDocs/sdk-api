---
UID: NF:msctf.ITfCategoryMgr.RegisterGUIDDWORD
title: ITfCategoryMgr::RegisterGUIDDWORD (msctf.h)
author: windows-sdk-content
description: ITfCategoryMgr::RegisterGUIDDWORD method
old-location: tsf\itfcategorymgr_registerguiddword.htm
tech.root: TSF
ms.assetid: 674165f4-1624-46fa-b3c6-ee5242fa457b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],RegisterGUIDDWORD method, ITfCategoryMgr.RegisterGUIDDWORD, ITfCategoryMgr::RegisterGUIDDWORD, RegisterGUIDDWORD, RegisterGUIDDWORD method [Text Services Framework], RegisterGUIDDWORD method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_registerguiddword_ref, msctf/ITfCategoryMgr::RegisterGUIDDWORD, tsf.itfcategorymgr_registerguiddword
ms.topic: method
f1_keywords: 
 - "msctf/ITfCategoryMgr.RegisterGUIDDWORD"
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
 - ITfCategoryMgr.RegisterGUIDDWORD
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCategoryMgr::RegisterGUIDDWORD


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the GUID.


### -param rguid [in]

Contains the GUID that the <b>DWORD</b> is registered for.


### -param dw [in]

Contains the <b>DWORD</b> value registered for the GUID.


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
The method was unable to register the <b>DWORD</b> value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcategorymgr">ITfCategoryMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-getguiddword">ITfCategoryMgr::GetGUIDDWORD
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-unregisterguiddword">ITfCategoryMgr::UnregisterGUIDDWORD
      </a>
 

 

