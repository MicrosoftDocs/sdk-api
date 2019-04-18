---
UID: NF:msctf.ITfCategoryMgr.UnregisterGUIDDescription
title: ITfCategoryMgr::UnregisterGUIDDescription (msctf.h)
author: windows-sdk-content
description: ITfCategoryMgr::UnregisterGUIDDescription method
old-location: tsf\itfcategorymgr_unregisterguiddescription.htm
tech.root: TSF
ms.assetid: 42bc1ddc-9f11-40dc-849c-2effc6efe1c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],UnregisterGUIDDescription method, ITfCategoryMgr.UnregisterGUIDDescription, ITfCategoryMgr::UnregisterGUIDDescription, UnregisterGUIDDescription, UnregisterGUIDDescription method [Text Services Framework], UnregisterGUIDDescription method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_unregisterguiddescription_ref, msctf/ITfCategoryMgr::UnregisterGUIDDescription, tsf.itfcategorymgr_unregisterguiddescription
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
 - ITfCategoryMgr.UnregisterGUIDDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCategoryMgr::UnregisterGUIDDescription


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the GUID.


### -param rguid [in]

Contains the GUID that the description is removed for.


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



<a href="https://msdn.microsoft.com/e0c4f64e-7e20-4dff-b597-acc280aebf32">ITfCategoryMgr::GetGUIDDescription
      </a>



<a href="https://msdn.microsoft.com/cb42e583-af5b-42ba-9637-889c7d4bdc82">ITfCategoryMgr::RegisterGUIDDescription
      </a>
 

 

