---
UID: NF:msctf.ITfCategoryMgr.UnregisterCategory
title: ITfCategoryMgr::UnregisterCategory
author: windows-sdk-content
description: ITfCategoryMgr::UnregisterCategory method
old-location: tsf\itfcategorymgr_unregistercategory.htm
old-project: TSF
ms.assetid: 73013bc1-4623-4e00-b87b-29ea3d728e9f
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],UnregisterCategory method, ITfCategoryMgr.UnregisterCategory, ITfCategoryMgr::UnregisterCategory, UnregisterCategory, UnregisterCategory method [Text Services Framework], UnregisterCategory method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_unregistercategory_ref, msctf/ITfCategoryMgr::UnregisterCategory, tsf.itfcategorymgr_unregistercategory
ms.prod: windows
ms.technology: windows-sdk
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
 - ITfCategoryMgr.UnregisterCategory
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCategoryMgr::UnregisterCategory


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the item.


### -param rcatid [in]

Contains a GUID that identifies the category that the item is registered under.


### -param rguid [in]

Contains a GUID that identifies the item to remove.


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



<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">
        ITfCategoryMgr::RegisterCategory
      </a>
 

 

