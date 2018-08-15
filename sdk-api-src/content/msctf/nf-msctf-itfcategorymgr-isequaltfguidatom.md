---
UID: NF:msctf.ITfCategoryMgr.IsEqualTfGuidAtom
title: ITfCategoryMgr::IsEqualTfGuidAtom
author: windows-sdk-content
description: ITfCategoryMgr::IsEqualTfGuidAtom method
old-location: tsf\itfcategorymgr_isequaltfguidatom.htm
old-project: TSF
ms.assetid: 813916f6-610f-4031-bb17-67d7f5ffed6f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],IsEqualTfGuidAtom method, ITfCategoryMgr.IsEqualTfGuidAtom, ITfCategoryMgr::IsEqualTfGuidAtom, IsEqualTfGuidAtom, IsEqualTfGuidAtom method [Text Services Framework], IsEqualTfGuidAtom method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_isequaltfguidatom_ref, msctf/ITfCategoryMgr::IsEqualTfGuidAtom, tsf.itfcategorymgr_isequaltfguidatom
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
 - ITfCategoryMgr.IsEqualTfGuidAtom
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCategoryMgr::IsEqualTfGuidAtom


## -description




## -parameters




### -param guidatom [in]

Specifies an atom that represents a GUID in the internal table.


### -param rguid [in]

Specifies the address of the GUID to compare with the atom in the internal table.


### -param pfEqual [out]

Pointer to a Boolean variable that receives an indication of whether the atom represents the GUID.


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
The method cannot access the internal table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>pfEqual</i> parameter was <b>NULL</b> on input.

</td>
</tr>
</table>
 




## -remarks



If the atom specified by the <i>guidatom</i> parameter represents the <b>GUID</b> specified by the <i>rguid</i> parameter, the <i>pfEqual</i> parameter receives a nonzero value. Otherwise, the <i>pfEqual</i> parameter receives zero.




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr</a>



<a href="https://msdn.microsoft.com/a5f5a67c-3152-4933-8a35-0a0cd555a0bf">ITfCategoryMgr::GetGUID</a>



<a href="https://msdn.microsoft.com/d0de17d9-be3a-4f68-a77d-880047775952">ITfCategoryMgr::RegisterGUID</a>
 

 

