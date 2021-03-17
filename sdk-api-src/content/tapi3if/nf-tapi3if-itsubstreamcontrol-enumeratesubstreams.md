---
UID: NF:tapi3if.ITSubStreamControl.EnumerateSubStreams
title: ITSubStreamControl::EnumerateSubStreams (tapi3if.h)
description: The EnumerateSubStreams method enumerates currently available media substreams. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the get_SubStreams method.
helpviewer_keywords: ["EnumerateSubStreams","EnumerateSubStreams method [TAPI 2.2]","EnumerateSubStreams method [TAPI 2.2]","ITSubStreamControl interface","ITSubStreamControl interface [TAPI 2.2]","EnumerateSubStreams method","ITSubStreamControl.EnumerateSubStreams","ITSubStreamControl::EnumerateSubStreams","_tapi3_itsubstreamcontrol_enumeratesubstreams","tapi3.itsubstreamcontrol_enumeratesubstreams","tapi3if/ITSubStreamControl::EnumerateSubStreams"]
old-location: tapi3\itsubstreamcontrol_enumeratesubstreams.htm
tech.root: tapi3
ms.assetid: 848d31e8-f878-4d33-b2b9-2d28e96bd14a
ms.date: 12/05/2018
ms.keywords: EnumerateSubStreams, EnumerateSubStreams method [TAPI 2.2], EnumerateSubStreams method [TAPI 2.2],ITSubStreamControl interface, ITSubStreamControl interface [TAPI 2.2],EnumerateSubStreams method, ITSubStreamControl.EnumerateSubStreams, ITSubStreamControl::EnumerateSubStreams, _tapi3_itsubstreamcontrol_enumeratesubstreams, tapi3.itsubstreamcontrol_enumeratesubstreams, tapi3if/ITSubStreamControl::EnumerateSubStreams
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
 - ITSubStreamControl::EnumerateSubStreams
 - tapi3if/ITSubStreamControl::EnumerateSubStreams
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
 - ITSubStreamControl.EnumerateSubStreams
---

# ITSubStreamControl::EnumerateSubStreams


## -description

The 
<b>EnumerateSubStreams</b> method enumerates currently available media substreams. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-get_substreams">get_SubStreams</a> method.

## -parameters

### -param ppEnumSubStream [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream">IEnumSubStream</a> enumeration of substreams.

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
The <i>ppEnumSubStream</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream">IEnumSubStream</a> interface returned by <b>ITSubStreamControl::EnumerateSubStreams</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumSubStream</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>