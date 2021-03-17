---
UID: NF:tapi3if.ITSubStreamControl.get_SubStreams
title: ITSubStreamControl::get_SubStreams (tapi3if.h)
description: The get_SubStreams method creates a collection of substreams currently available. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateSubStreams method.
helpviewer_keywords: ["ITSubStreamControl interface [TAPI 2.2]","get_SubStreams method","ITSubStreamControl.get_SubStreams","ITSubStreamControl::get_SubStreams","_tapi3_itsubstreamcontrol_get_substreams","get_SubStreams","get_SubStreams method [TAPI 2.2]","get_SubStreams method [TAPI 2.2]","ITSubStreamControl interface","tapi3.itsubstreamcontrol_get_substreams","tapi3if/ITSubStreamControl::get_SubStreams"]
old-location: tapi3\itsubstreamcontrol_get_substreams.htm
tech.root: tapi3
ms.assetid: 1ea7dca0-9a0b-4966-83ba-0d1f6c5e5ccb
ms.date: 12/05/2018
ms.keywords: ITSubStreamControl interface [TAPI 2.2],get_SubStreams method, ITSubStreamControl.get_SubStreams, ITSubStreamControl::get_SubStreams, _tapi3_itsubstreamcontrol_get_substreams, get_SubStreams, get_SubStreams method [TAPI 2.2], get_SubStreams method [TAPI 2.2],ITSubStreamControl interface, tapi3.itsubstreamcontrol_get_substreams, tapi3if/ITSubStreamControl::get_SubStreams
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSubStreamControl::get_SubStreams
 - tapi3if/ITSubStreamControl::get_SubStreams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITSubStreamControl.get_SubStreams
---

# ITSubStreamControl::get_SubStreams


## -description

The 
<b>get_SubStreams</b> method creates a collection of substreams currently available. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-enumeratesubstreams">EnumerateSubStreams</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a> interface pointers.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The call appears to have been shut down.

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

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a> interface returned by <b>ITSubStreamControl::get_SubStreams</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITSubStream</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubstream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>