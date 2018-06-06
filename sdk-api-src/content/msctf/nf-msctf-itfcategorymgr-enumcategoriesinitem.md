---
UID: NF:msctf.ITfCategoryMgr.EnumCategoriesInItem
title: ITfCategoryMgr::EnumCategoriesInItem
author: windows-sdk-content
description: ITfCategoryMgr::EnumCategoriesInItem method
old-location: tsf\itfcategorymgr_enumcategoriesinitem.htm
old-project: TSF
ms.assetid: 271e5fbe-54e2-47e3-97d4-cd4211b92080
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: EnumCategoriesInItem, EnumCategoriesInItem method [Text Services Framework], EnumCategoriesInItem method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],EnumCategoriesInItem method, ITfCategoryMgr.EnumCategoriesInItem, ITfCategoryMgr::EnumCategoriesInItem, _tsf_itfcategorymgr_enumcategoriesinitem_ref, msctf/ITfCategoryMgr::EnumCategoriesInItem, tsf.itfcategorymgr_enumcategoriesinitem
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
 - ITfCategoryMgr.EnumCategoriesInItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCategoryMgr::EnumCategoriesInItem


## -description




## -parameters




### -param rguid [in]

Contains a GUID value that identifies the item to enumerate the categories for.


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



<a href="https://msdn.microsoft.com/88b123d8-86aa-40ae-8777-1b33cfbb953a">
        ITfCategoryMgr::EnumItemsInCategory
      </a>



<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">
        ITfCategoryMgr::RegisterCategory
      </a>
 

 

