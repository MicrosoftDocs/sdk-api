---
UID: NF:msctf.ITfCategoryMgr.RegisterGUIDDescription
title: ITfCategoryMgr::RegisterGUIDDescription (msctf.h)
author: windows-sdk-content
description: ITfCategoryMgr::RegisterGUIDDescription method
old-location: tsf\itfcategorymgr_registerguiddescription.htm
tech.root: TSF
ms.assetid: cb42e583-af5b-42ba-9637-889c7d4bdc82
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],RegisterGUIDDescription method, ITfCategoryMgr.RegisterGUIDDescription, ITfCategoryMgr::RegisterGUIDDescription, RegisterGUIDDescription, RegisterGUIDDescription method [Text Services Framework], RegisterGUIDDescription method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_registerguiddescription_ref, msctf/ITfCategoryMgr::RegisterGUIDDescription, tsf.itfcategorymgr_registerguiddescription
ms.topic: method
f1_keywords: 
 - "msctf/ITfCategoryMgr.RegisterGUIDDescription"
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
 - ITfCategoryMgr.RegisterGUIDDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCategoryMgr::RegisterGUIDDescription


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the GUID.


### -param rguid [in]

Contains the GUID that the description is registered for.


### -param pchDesc [in]

Pointer to a <b>WCHAR</b> buffer that contains the description for the GUID.


### -param cch [in]

Contains the length, in characters, of the description string.


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
The method was unable to register the description string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pchDest</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcategorymgr">ITfCategoryMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-getguiddescription">ITfCategoryMgr::GetGUIDDescription
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-unregisterguiddescription">ITfCategoryMgr::UnregisterGUIDDescription
      </a>
 

 

