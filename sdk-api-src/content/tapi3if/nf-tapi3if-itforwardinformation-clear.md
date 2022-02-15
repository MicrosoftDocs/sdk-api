---
UID: NF:tapi3if.ITForwardInformation.Clear
title: ITForwardInformation::Clear (tapi3if.h)
description: The Clear method clears all forwarding information in this object.
helpviewer_keywords: ["Clear","Clear method [TAPI 2.2]","Clear method [TAPI 2.2]","ITForwardInformation interface","ITForwardInformation interface [TAPI 2.2]","Clear method","ITForwardInformation.Clear","ITForwardInformation::Clear","_tapi3_itforwardinformation_clear","tapi3.itforwardinformation_clear","tapi3if/ITForwardInformation::Clear"]
old-location: tapi3\itforwardinformation_clear.htm
tech.root: tapi3
ms.assetid: 721a4efc-e379-4553-a2a1-efb8831cda38
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [TAPI 2.2], Clear method [TAPI 2.2],ITForwardInformation interface, ITForwardInformation interface [TAPI 2.2],Clear method, ITForwardInformation.Clear, ITForwardInformation::Clear, _tapi3_itforwardinformation_clear, tapi3.itforwardinformation_clear, tapi3if/ITForwardInformation::Clear
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
 - ITForwardInformation::Clear
 - tapi3if/ITForwardInformation::Clear
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
 - ITForwardInformation.Clear
---

# ITForwardInformation::Clear


## -description

The 
<b>Clear</b> method clears all forwarding information in this object.



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

## -remarks

This method does not clear forwarding information in the service provider.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
