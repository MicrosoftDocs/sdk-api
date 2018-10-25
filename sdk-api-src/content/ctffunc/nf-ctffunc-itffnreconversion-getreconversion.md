---
UID: NF:ctffunc.ITfFnReconversion.GetReconversion
title: ITfFnReconversion::GetReconversion
author: windows-sdk-content
description: ITfFnReconversion::GetReconversion method
old-location: tsf\itffnreconversion_getreconversion.htm
tech.root: TSF
ms.assetid: ed696088-c599-4c83-968e-d09d9ae81c10
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetReconversion, GetReconversion method [Text Services Framework], GetReconversion method [Text Services Framework],ITfFnReconversion interface, ITfFnReconversion interface [Text Services Framework],GetReconversion method, ITfFnReconversion.GetReconversion, ITfFnReconversion::GetReconversion, _tsf_itffnreconversion_getreconversion_ref, ctffunc/ITfFnReconversion::GetReconversion, tsf.itffnreconversion_getreconversion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfFnReconversion.GetReconversion
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnReconversion::GetReconversion


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628908(v=VS.85).aspx">ITfRange</a> object that covers the text to be reconverted. This range object is obtained by calling <a href="https://msdn.microsoft.com/en-us/library/ms538973(v=VS.85).aspx">ITfFnReconversion::QueryRange</a>.


### -param ppCandList [out]

Pointer to an <b>ITfCandidateList</b> pointer that receives the candidate list object.


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
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e41ba461-6337-4feb-ba16-3942920ebb9f">ITfCandidateList
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms538970(v=VS.85).aspx">ITfFnReconversion</a>



<a href="https://msdn.microsoft.com/022d0ad7-5359-48df-b83b-2319eb1a84bf">ITfFnReconversion::QueryRange
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

