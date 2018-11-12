---
UID: NF:ctffunc.ITfFnAdviseText.OnLatticeUpdate
title: ITfFnAdviseText::OnLatticeUpdate
author: windows-sdk-content
description: ITfFnAdviseText::OnLatticeUpdate method
old-location: tsf\itffnadvisetext_onlatticeupdate.htm
tech.root: TSF
ms.assetid: c58f3d2f-ad74-43a7-a8a8-65d65d603611
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfFnAdviseText interface [Text Services Framework],OnLatticeUpdate method, ITfFnAdviseText.OnLatticeUpdate, ITfFnAdviseText::OnLatticeUpdate, OnLatticeUpdate, OnLatticeUpdate method [Text Services Framework], OnLatticeUpdate method [Text Services Framework],ITfFnAdviseText interface, _tsf_itffnadvisetext_onlatticeupdate_ref, ctffunc/ITfFnAdviseText::OnLatticeUpdate, tsf.itffnadvisetext_onlatticeupdate
ms.prod: windows-hardware
ms.technology: windows-devices
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

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628908(v=VS.85).aspx">ITfRange</a> object that represents the range of text that changed.


### -param pLattice [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628774(v=VS.85).aspx">ITfLMLattice</a> object that represents the new lattice element.


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




<a href="https://msdn.microsoft.com/en-us/library/ms538915(v=VS.85).aspx">ITfFnAdviseText</a>



<a href="https://msdn.microsoft.com/en-us/library/ms628774(v=VS.85).aspx">ITfLMLattice</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

