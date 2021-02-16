---
UID: NF:wsdbase.IWSDUdpMessageParameters.SetRetransmitParams
title: IWSDUdpMessageParameters::SetRetransmitParams (wsdbase.h)
description: Sets the values that WSD uses to determine how often to repeat the message transmission.
helpviewer_keywords: ["IWSDUdpMessageParameters interface","SetRetransmitParams method","IWSDUdpMessageParameters.SetRetransmitParams","IWSDUdpMessageParameters::SetRetransmitParams","SetRetransmitParams","SetRetransmitParams method","SetRetransmitParams method","IWSDUdpMessageParameters interface","ncd.iwsdudpmessageparameters_setretransmitparams","wsdbase/IWSDUdpMessageParameters::SetRetransmitParams"]
old-location: ncd\iwsdudpmessageparameters_setretransmitparams.htm
tech.root: ncd
ms.assetid: 8fef8dc9-7621-4928-94a6-491a095b11fa
ms.date: 12/05/2018
ms.keywords: IWSDUdpMessageParameters interface,SetRetransmitParams method, IWSDUdpMessageParameters.SetRetransmitParams, IWSDUdpMessageParameters::SetRetransmitParams, SetRetransmitParams, SetRetransmitParams method, SetRetransmitParams method,IWSDUdpMessageParameters interface, ncd.iwsdudpmessageparameters_setretransmitparams, wsdbase/IWSDUdpMessageParameters::SetRetransmitParams
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
 - IWSDUdpMessageParameters::SetRetransmitParams
 - wsdbase/IWSDUdpMessageParameters::SetRetransmitParams
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
 - IWSDUdpMessageParameters.SetRetransmitParams
---

# IWSDUdpMessageParameters::SetRetransmitParams


## -description

Sets the values that WSD uses to determine how often to repeat the message transmission.

## -parameters

### -param pParams [in]

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
</table>

## -remarks

If you do not specify these values, WSD sends the message only once.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpmessageparameters">IWSDUdpMessageParameters</a>