---
UID: NF:tapi3.ITMSPAddress.ShutdownMSPCall
title: ITMSPAddress::ShutdownMSPCall (tapi3.h)
description: The ITMSPAddress::ShutdownMSPCall (tapi3.h) method is called when the call object is being destroyed.
helpviewer_keywords: ["ITMSPAddress interface [TAPI 2.2]","ShutdownMSPCall method","ITMSPAddress.ShutdownMSPCall","ITMSPAddress::ShutdownMSPCall","ShutdownMSPCall","ShutdownMSPCall method [TAPI 2.2]","ShutdownMSPCall method [TAPI 2.2]","ITMSPAddress interface","_tapi3_itmspaddress_shutdownmspcall","msp/ITMSPAddress::ShutdownMSPCall","tapi3.itmspaddress_shutdownmspcall"]
old-location: tapi3\itmspaddress_shutdownmspcall.htm
tech.root: tapi3
ms.assetid: 6527db85-cad8-4b0d-977a-9ab8b047e44e
ms.date: 08/09/2022
ms.keywords: ITMSPAddress interface [TAPI 2.2],ShutdownMSPCall method, ITMSPAddress.ShutdownMSPCall, ITMSPAddress::ShutdownMSPCall, ShutdownMSPCall, ShutdownMSPCall method [TAPI 2.2], ShutdownMSPCall method [TAPI 2.2],ITMSPAddress interface, _tapi3_itmspaddress_shutdownmspcall, msp/ITMSPAddress::ShutdownMSPCall, tapi3.itmspaddress_shutdownmspcall
req.header: tapi3.h
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
 - ITMSPAddress::ShutdownMSPCall
 - tapi3/ITMSPAddress::ShutdownMSPCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress.ShutdownMSPCall
---

# ITMSPAddress::ShutdownMSPCall


## -description

The 
<b>ShutdownMSPCall</b> method is called when the call object is being destroyed.

## -parameters

### -param pStreamControl [in]

Pointer to <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for the call's 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>.

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
The <i>pStreamControl</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pStreamControl</i> parameter does not point to a valid 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a> interface.

</td>
</tr>
</table>

## -remarks

This method is not automatically invoked when a call enters the disconnect state. The paired TSP of the MSP should notify the MSP of this call state change, but, because applications may retain the call object for information logging purposes after a disconnect, shutdown should not be called until the call object itself is released.

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itmspaddress">ITMSPAddress</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
