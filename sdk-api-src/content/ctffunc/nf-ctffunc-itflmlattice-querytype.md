---
UID: NF:ctffunc.ITfLMLattice.QueryType
title: ITfLMLattice::QueryType (ctffunc.h)
description: ITfLMLattice::QueryType method
helpviewer_keywords: ["ITfLMLattice interface [Text Services Framework]","QueryType method","ITfLMLattice.QueryType","ITfLMLattice::QueryType","QueryType","QueryType method [Text Services Framework]","QueryType method [Text Services Framework]","ITfLMLattice interface","_tsf_itflmlattice_querytype_ref","ctffunc/ITfLMLattice::QueryType","tsf.itflmlattice_querytype"]
old-location: tsf\itflmlattice_querytype.htm
tech.root: TSF
ms.assetid: 199032f7-b97f-4475-9ce3-9af952e13f12
ms.date: 12/05/2018
ms.keywords: ITfLMLattice interface [Text Services Framework],QueryType method, ITfLMLattice.QueryType, ITfLMLattice::QueryType, QueryType, QueryType method [Text Services Framework], QueryType method [Text Services Framework],ITfLMLattice interface, _tsf_itflmlattice_querytype_ref, ctffunc/ITfLMLattice::QueryType, tsf.itflmlattice_querytype
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfLMLattice::QueryType
 - ctffunc/ITfLMLattice::QueryType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfLMLattice.QueryType
---

# ITfLMLattice::QueryType


## -description

Determines if a specific lattice element type is supported by the lattice property.

## -parameters

### -param rguidType [in]

Specifies the lattice type identifier. This can be one of the <a href="/windows/desktop/TSF/lattice-types">Lattice Type</a> values.

### -param pfSupported [out]

Pointer to a <b>BOOL</b> that receives a value that indicates if the lattice type is supported. If the lattice type is supported, this parameter receives a nonzero value and the method returns S_OK. If the lattice type is unsupported, this parameter receives zero and the method returns E_INVALIDARG.

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
The specified lattice type is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Either <i>pfSupported</i> is invalid or the specified lattice type is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itflmlattice">ITfLMLattice</a>



<a href="/windows/desktop/TSF/lattice-types">Lattice Types
      </a>