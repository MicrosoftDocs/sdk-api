---
UID: NF:ctffunc.ITfFnReconversion.Reconvert
title: ITfFnReconversion::Reconvert
author: windows-sdk-content
description: ITfFnReconversion::Reconvert method
old-location: tsf\itffnreconversion_reconvert.htm
tech.root: TSF
ms.assetid: 81d0f376-c059-4fcf-b85b-645bc98f957d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfFnReconversion interface [Text Services Framework],Reconvert method, ITfFnReconversion.Reconvert, ITfFnReconversion::Reconvert, Reconvert, Reconvert method [Text Services Framework], Reconvert method [Text Services Framework],ITfFnReconversion interface, _tsf_itffnreconversion_reconvert_ref, ctffunc/ITfFnReconversion::Reconvert, tsf.itffnreconversion_reconvert
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
 - ITfFnReconversion.Reconvert
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnReconversion::Reconvert


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628908(v=VS.85).aspx">ITfRange</a> object that covers the text to be reconverted. To obtain this range object call <a href="https://msdn.microsoft.com/en-us/library/ms538973(v=VS.85).aspx">ITfFnReconversion::QueryRange</a>.


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
 




## -remarks



If this method causes some type of user interface to be displayed, such as a dialog box, this method must not wait for the UI to be dismissed before returning.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms538970(v=VS.85).aspx">ITfFnReconversion</a>



<a href="https://msdn.microsoft.com/022d0ad7-5359-48df-b83b-2319eb1a84bf">ITfFnReconversion::QueryRange
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

