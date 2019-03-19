---
UID: NF:ctffunc.ITfFnAdviseText.OnLatticeUpdate
title: ITfFnAdviseText::OnLatticeUpdate (ctffunc.h)
author: windows-sdk-content
description: ITfFnAdviseText::OnLatticeUpdate method
old-location: tsf\itffnadvisetext_onlatticeupdate.htm
tech.root: TSF
ms.assetid: c58f3d2f-ad74-43a7-a8a8-65d65d603611
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfFnAdviseText interface [Text Services Framework],OnLatticeUpdate method, ITfFnAdviseText.OnLatticeUpdate, ITfFnAdviseText::OnLatticeUpdate, OnLatticeUpdate, OnLatticeUpdate method [Text Services Framework], OnLatticeUpdate method [Text Services Framework],ITfFnAdviseText interface, _tsf_itffnadvisetext_onlatticeupdate_ref, ctffunc/ITfFnAdviseText::OnLatticeUpdate, tsf.itffnadvisetext_onlatticeupdate
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - Msctf.dll
api_name:
 - ITfFnAdviseText.OnLatticeUpdate
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnAdviseText::OnLatticeUpdate


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that represents the range of text that changed.


### -param pLattice [in]

Pointer to an <a href="https://msdn.microsoft.com/25ad6ef2-1d42-498a-852f-163a0efbc26a">ITfLMLattice</a> object that represents the new lattice element.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7cca7f23-48d3-4855-8f3d-e937bbc990d4">ITfFnAdviseText</a>



<a href="https://msdn.microsoft.com/25ad6ef2-1d42-498a-852f-163a0efbc26a">ITfLMLattice</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

