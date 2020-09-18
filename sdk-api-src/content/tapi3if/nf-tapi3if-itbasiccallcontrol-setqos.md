---
UID: NF:tapi3if.ITBasicCallControl.SetQOS
title: ITBasicCallControl::SetQOS (tapi3if.h)
description: The SetQOS method sets the quality of service level for the call.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","SetQOS method","ITBasicCallControl.SetQOS","ITBasicCallControl::SetQOS","SetQOS","SetQOS method [TAPI 2.2]","SetQOS method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_setqos","tapi3.itbasiccallcontrol_setqos","tapi3if/ITBasicCallControl::SetQOS"]
old-location: tapi3\itbasiccallcontrol_setqos.htm
tech.root: tapi3
ms.assetid: f1e6ef32-5706-4b1c-a1fa-a7be48fd6efd
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],SetQOS method, ITBasicCallControl.SetQOS, ITBasicCallControl::SetQOS, SetQOS, SetQOS method [TAPI 2.2], SetQOS method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_setqos, tapi3.itbasiccallcontrol_setqos, tapi3if/ITBasicCallControl::SetQOS
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
 - ITBasicCallControl::SetQOS
 - tapi3if/ITBasicCallControl::SetQOS
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
 - ITBasicCallControl.SetQOS
---

# ITBasicCallControl::SetQOS


## -description

The 
<b>SetQOS</b> method sets the quality of service level for the call.

## -parameters

### -param lMediaType [in]

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a> of call.

### -param ServiceLevel [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-qos_service_level">QOS_SERVICE_LEVEL</a> indicator of desired QOS level for call.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not a valid media type.

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

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-qos_service_level">QOS_SERVICE_LEVEL</a>