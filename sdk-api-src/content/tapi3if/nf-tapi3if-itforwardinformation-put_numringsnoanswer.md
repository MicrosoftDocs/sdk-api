---
UID: NF:tapi3if.ITForwardInformation.put_NumRingsNoAnswer
title: ITForwardInformation::put_NumRingsNoAnswer (tapi3if.h)
description: The put_NumRingsNoAnswer method sets the number of rings after which a no answer condition is assumed.
helpviewer_keywords: ["ITForwardInformation interface [TAPI 2.2]","put_NumRingsNoAnswer method","ITForwardInformation.put_NumRingsNoAnswer","ITForwardInformation::put_NumRingsNoAnswer","_tapi3_itforwardinformation_put_numringsnoanswer","put_NumRingsNoAnswer","put_NumRingsNoAnswer method [TAPI 2.2]","put_NumRingsNoAnswer method [TAPI 2.2]","ITForwardInformation interface","tapi3.itforwardinformation_put_numringsnoanswer","tapi3if/ITForwardInformation::put_NumRingsNoAnswer"]
old-location: tapi3\itforwardinformation_put_numringsnoanswer.htm
tech.root: tapi3
ms.assetid: ad7b2746-cb97-406e-a328-efc051681aa6
ms.date: 12/05/2018
ms.keywords: ITForwardInformation interface [TAPI 2.2],put_NumRingsNoAnswer method, ITForwardInformation.put_NumRingsNoAnswer, ITForwardInformation::put_NumRingsNoAnswer, _tapi3_itforwardinformation_put_numringsnoanswer, put_NumRingsNoAnswer, put_NumRingsNoAnswer method [TAPI 2.2], put_NumRingsNoAnswer method [TAPI 2.2],ITForwardInformation interface, tapi3.itforwardinformation_put_numringsnoanswer, tapi3if/ITForwardInformation::put_NumRingsNoAnswer
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
 - ITForwardInformation::put_NumRingsNoAnswer
 - tapi3if/ITForwardInformation::put_NumRingsNoAnswer
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
 - ITForwardInformation.put_NumRingsNoAnswer
---

# ITForwardInformation::put_NumRingsNoAnswer


## -description

The 
<b>put_NumRingsNoAnswer</b> method sets the number of rings after which a no answer condition is assumed.

## -parameters

### -param lNumRings [in]

Number of rings.

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
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-get_numringsnoanswer">get_NumRingsNoAnswer</a>