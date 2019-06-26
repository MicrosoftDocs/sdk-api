---
UID: NF:msctf.ITfCategoryMgr.IsEqualTfGuidAtom
title: ITfCategoryMgr::IsEqualTfGuidAtom (msctf.h)
author: windows-sdk-content
description: ITfCategoryMgr::IsEqualTfGuidAtom method
old-location: tsf\itfcategorymgr_isequaltfguidatom.htm
tech.root: TSF
ms.assetid: 813916f6-610f-4031-bb17-67d7f5ffed6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],IsEqualTfGuidAtom method, ITfCategoryMgr.IsEqualTfGuidAtom, ITfCategoryMgr::IsEqualTfGuidAtom, IsEqualTfGuidAtom, IsEqualTfGuidAtom method [Text Services Framework], IsEqualTfGuidAtom method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_isequaltfguidatom_ref, msctf/ITfCategoryMgr::IsEqualTfGuidAtom, tsf.itfcategorymgr_isequaltfguidatom
ms.topic: method
f1_keywords: 
 - "msctf/ITfCategoryMgr.IsEqualTfGuidAtom"
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
 - ITfCategoryMgr.IsEqualTfGuidAtom
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcategorymgr">ITfCategoryMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-getguid">ITfCategoryMgr::GetGUID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registerguid">ITfCategoryMgr::RegisterGUID</a>
 

 

