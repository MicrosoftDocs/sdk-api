---
UID: NF:msctf.ITfCategoryMgr.RegisterGUIDDescription
title: ITfCategoryMgr::RegisterGUIDDescription
author: windows-sdk-content
description: ITfCategoryMgr::RegisterGUIDDescription method
old-location: tsf\itfcategorymgr_registerguiddescription.htm
old-project: TSF
ms.assetid: cb42e583-af5b-42ba-9637-889c7d4bdc82
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],RegisterGUIDDescription method, ITfCategoryMgr.RegisterGUIDDescription, ITfCategoryMgr::RegisterGUIDDescription, RegisterGUIDDescription, RegisterGUIDDescription method [Text Services Framework], RegisterGUIDDescription method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_registerguiddescription_ref, msctf/ITfCategoryMgr::RegisterGUIDDescription, tsf.itfcategorymgr_registerguiddescription
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/e0c4f64e-7e20-4dff-b597-acc280aebf32">ITfCategoryMgr::GetGUIDDescription
      </a>



<a href="https://msdn.microsoft.com/42bc1ddc-9f11-40dc-849c-2effc6efe1c8">ITfCategoryMgr::UnregisterGUIDDescription
      </a>
 

 

