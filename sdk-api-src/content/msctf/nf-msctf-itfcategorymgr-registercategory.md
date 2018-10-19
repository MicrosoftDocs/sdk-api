---
UID: NF:msctf.ITfCategoryMgr.RegisterCategory
title: ITfCategoryMgr::RegisterCategory
author: windows-sdk-content
description: ITfCategoryMgr::RegisterCategory method
old-location: tsf\itfcategorymgr_registercategory.htm
tech.root: TSF
ms.assetid: 9e9a72a8-ea9b-4438-992c-5a7db64f7d82
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],RegisterCategory method, ITfCategoryMgr.RegisterCategory, ITfCategoryMgr::RegisterCategory, RegisterCategory, RegisterCategory method [Text Services Framework], RegisterCategory method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_registercategory_ref, msctf/ITfCategoryMgr::RegisterCategory, tsf.itfcategorymgr_registercategory
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
 - ITfCategoryMgr.RegisterCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCategoryMgr::RegisterCategory


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the item.


### -param rcatid [in]

Contains a GUID value that identifies the category to register the item under. This can be a user-defined category or one of the <a href="https://msdn.microsoft.com/04c0632d-ac64-4081-ba95-c11feb3f40dd">predefined category values</a>.


### -param rguid [in]

Contains a GUID value that identifies the item to register.


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
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/73013bc1-4623-4e00-b87b-29ea3d728e9f">ITfCategoryMgr::UnregisterCategory
      </a>



<a href="https://msdn.microsoft.com/04c0632d-ac64-4081-ba95-c11feb3f40dd">Predefined Category Values
      </a>
 

 

