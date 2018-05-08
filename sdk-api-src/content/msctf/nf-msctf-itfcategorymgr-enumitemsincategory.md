---
UID: NF:msctf.ITfCategoryMgr.EnumItemsInCategory
title: ITfCategoryMgr::EnumItemsInCategory
author: windows-driver-content
description: ITfCategoryMgr::EnumItemsInCategory method
old-location: tsf\itfcategorymgr_enumitemsincategory.htm
old-project: TSF
ms.assetid: 88b123d8-86aa-40ae-8777-1b33cfbb953a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: EnumItemsInCategory, EnumItemsInCategory method [Text Services Framework], EnumItemsInCategory method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],EnumItemsInCategory method, ITfCategoryMgr.EnumItemsInCategory, ITfCategoryMgr::EnumItemsInCategory, _tsf_itfcategorymgr_enumitemsincategory_ref, msctf/ITfCategoryMgr::EnumItemsInCategory, tsf.itfcategorymgr_enumitemsincategory
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
-	msctf.dll
api_name:
-	ITfCategoryMgr.EnumItemsInCategory
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCategoryMgr::EnumItemsInCategory


## -description




## -parameters




### -param rcatid [in]

Contains a GUID value that identifies the category to enumerate the items for.


### -param ppEnum [out]

Pointer to an IEnumGUID interface pointer that receives the enumerator.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEnum</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/271e5fbe-54e2-47e3-97d4-cd4211b92080">
        ITfCategoryMgr::EnumCategoriesInItem
      </a>



<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">
        ITfCategoryMgr::RegisterCategory
      </a>
 

 

