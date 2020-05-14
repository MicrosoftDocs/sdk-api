---
UID: NF:tapi3if.ITPhone.NegotiateExtVersion
title: ITPhone::NegotiateExtVersion (tapi3if.h)
description: The NegotiateExtVersion method allows an application to negotiate an extension version to use with the specified phone device. This operation need not be called if the application does not support provider specific extensions.helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","NegotiateExtVersion method","ITPhone.NegotiateExtVersion","ITPhone::NegotiateExtVersion","NegotiateExtVersion","NegotiateExtVersion method [TAPI 2.2]","NegotiateExtVersion method [TAPI 2.2]","ITPhone interface","_tapi3_itphone_negotiateextversion","tapi3.itphone_negotiateextversion","tapi3if/ITPhone::NegotiateExtVersion"]
old-location: tapi3\itphone_negotiateextversion.htm
tech.root: Tapi
ms.assetid: a29311bf-0fe4-4e58-96cc-2e3734c32aee
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],NegotiateExtVersion method, ITPhone.NegotiateExtVersion, ITPhone::NegotiateExtVersion, NegotiateExtVersion, NegotiateExtVersion method [TAPI 2.2], NegotiateExtVersion method [TAPI 2.2],ITPhone interface, _tapi3_itphone_negotiateextversion, tapi3.itphone_negotiateextversion, tapi3if/ITPhone::NegotiateExtVersion
f1_keywords:
- tapi3if/ITPhone.NegotiateExtVersion
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITPhone.NegotiateExtVersion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhone::NegotiateExtVersion


## -description


The 
<b>NegotiateExtVersion</b> method allows an application to negotiate an extension version to use with the specified phone device. This operation need not be called if the application does not support provider specific extensions.


## -parameters




### -param lLowVersion [in]

Least recent extension version of the extension identifier returned by 
<b>NegotiateExtVersion</b> that the application is compliant with. The high-order word is the major version number; the low-order word is the minor version number.


### -param lHighVersion [in]

Most recent extension version of the extension identifier returned by 
<b>NegotiateExtVersion</b> that the application is compliant with. The high-order word is the major version number; the low-order word is the minor version number.


### -param plExtVersion [out]

Pointer to a <b>long</b> that contains the extension version number that was negotiated. If negotiation succeeds, this number is in the range between <i>lLowVersion</i> and <i>lHighVersion</i>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The version in <i>lHighVersion</i> or <i>lLowVersion</i> is invalid.

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
The <i>plExtVersion</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-devicespecific">DeviceSpecific</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-devicespecificvariant">DeviceSpecificVariant</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linenegotiateextversion">lineNegotiateExtVersion</a>
 

 

