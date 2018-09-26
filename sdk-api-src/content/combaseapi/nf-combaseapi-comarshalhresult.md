---
UID: NF:combaseapi.CoMarshalHresult
title: CoMarshalHresult function
author: windows-sdk-content
description: Marshals an HRESULT to the specified stream, from which it can be unmarshaled using the CoUnmarshalHresult function.
old-location: com\comarshalhresult.htm
tech.root: com
ms.assetid: 37aaf404-49ca-4881-a369-44c5288abf1d
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CoMarshalHresult, CoMarshalHresult function [COM], _com_CoMarshalHresult, com.comarshalhresult, combaseapi/CoMarshalHresult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoMarshalHresult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoMarshalHresult function


## -description


Marshals an <b>HRESULT</b> to the specified stream, from which it can be unmarshaled using the <a href="https://msdn.microsoft.com/a45ef72c-d385-4012-9683-7d2cc6d68b6d">CoUnmarshalHresult</a> function.




## -parameters




### -param pstm [in]

A pointer to the marshaling stream. See <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


### -param hresult [in]

The <b>HRESULT</b> in the originating process.


## -returns



This function can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The <b>HRESULT</b> was marshaled successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
A bad pointer was specified for <i>pstm</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
The medium is full.

</td>
</tr>
</table>
 




## -remarks



An <b>HRESULT</b> is process-specific, so an <b>HRESULT</b> that is valid in one process might not be valid in another. If you are writing your own implementation of <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> and need to marshal an <b>HRESULT</b> from one process to another, either as a parameter or a return code, you must call this function. In other circumstances, you will have no need to call this function.

This function performs the following tasks:

<ol>
<li>Writes an <b>HRESULT</b> to a stream.</li>
<li>Returns an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer to that stream.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/a45ef72c-d385-4012-9683-7d2cc6d68b6d">CoUnmarshalHresult</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

