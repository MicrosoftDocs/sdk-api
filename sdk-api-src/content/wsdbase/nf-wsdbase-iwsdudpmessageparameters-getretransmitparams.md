---
UID: NF:wsdbase.IWSDUdpMessageParameters.GetRetransmitParams
title: IWSDUdpMessageParameters::GetRetransmitParams (wsdbase.h)
description: Retrieves the values that WSD uses to determine how often to repeat the message transmission.
helpviewer_keywords: ["GetRetransmitParams","GetRetransmitParams method","GetRetransmitParams method","IWSDUdpMessageParameters interface","IWSDUdpMessageParameters interface","GetRetransmitParams method","IWSDUdpMessageParameters.GetRetransmitParams","IWSDUdpMessageParameters::GetRetransmitParams","ncd.iwsdudpmessageparameters_getretransmitparams","wsdbase/IWSDUdpMessageParameters::GetRetransmitParams"]
old-location: ncd\iwsdudpmessageparameters_getretransmitparams.htm
tech.root: ncd
ms.assetid: c34d6320-c70b-410e-ae21-fba849dac62f
ms.date: 12/05/2018
ms.keywords: GetRetransmitParams, GetRetransmitParams method, GetRetransmitParams method,IWSDUdpMessageParameters interface, IWSDUdpMessageParameters interface,GetRetransmitParams method, IWSDUdpMessageParameters.GetRetransmitParams, IWSDUdpMessageParameters::GetRetransmitParams, ncd.iwsdudpmessageparameters_getretransmitparams, wsdbase/IWSDUdpMessageParameters::GetRetransmitParams
req.header: wsdbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDUdpMessageParameters::GetRetransmitParams
 - wsdbase/IWSDUdpMessageParameters::GetRetransmitParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpMessageParameters.GetRetransmitParams
---

# IWSDUdpMessageParameters::GetRetransmitParams


## -description

Retrieves the values that WSD uses to determine how often to repeat the message transmission.

## -parameters

### -param pParams [out]

Pointer to a <a href="/windows/desktop/api/wsdbase/ns-wsdbase-wsdudpretransmitparams">WSDUdpRetransmitParams</a> structure. The structure contains values that determine how often WSD repeats the message transmission.

## -returns

Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pParams</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpmessageparameters">IWSDUdpMessageParameters</a>