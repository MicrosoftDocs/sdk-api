---
UID: NF:tapi3if.ITForwardInformation.get_NumRingsNoAnswer
title: ITForwardInformation::get_NumRingsNoAnswer (tapi3if.h)
description: The get_NumRingsNoAnswer method retrieves the number of rings after which a no answer condition is assumed.
helpviewer_keywords: ["ITForwardInformation interface [TAPI 2.2]","get_NumRingsNoAnswer method","ITForwardInformation.get_NumRingsNoAnswer","ITForwardInformation::get_NumRingsNoAnswer","_tapi3_itforwardinformation_get_numringsnoanswer","get_NumRingsNoAnswer","get_NumRingsNoAnswer method [TAPI 2.2]","get_NumRingsNoAnswer method [TAPI 2.2]","ITForwardInformation interface","tapi3.itforwardinformation_get_numringsnoanswer","tapi3if/ITForwardInformation::get_NumRingsNoAnswer"]
old-location: tapi3\itforwardinformation_get_numringsnoanswer.htm
tech.root: tapi3
ms.assetid: bfd46f8b-6501-43ca-b3bd-35394526d5ce
ms.date: 12/05/2018
ms.keywords: ITForwardInformation interface [TAPI 2.2],get_NumRingsNoAnswer method, ITForwardInformation.get_NumRingsNoAnswer, ITForwardInformation::get_NumRingsNoAnswer, _tapi3_itforwardinformation_get_numringsnoanswer, get_NumRingsNoAnswer, get_NumRingsNoAnswer method [TAPI 2.2], get_NumRingsNoAnswer method [TAPI 2.2],ITForwardInformation interface, tapi3.itforwardinformation_get_numringsnoanswer, tapi3if/ITForwardInformation::get_NumRingsNoAnswer
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITForwardInformation::get_NumRingsNoAnswer
 - tapi3if/ITForwardInformation::get_NumRingsNoAnswer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITForwardInformation.get_NumRingsNoAnswer
---

# ITForwardInformation::get_NumRingsNoAnswer


## -description

The 
<b>get_NumRingsNoAnswer</b> method retrieves the number of rings after which a no answer condition is assumed.

## -parameters

### -param plNumRings [out]

Pointer to number of rings.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plNumRings</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-put_numringsnoanswer">put_NumRingsNoAnswer</a>