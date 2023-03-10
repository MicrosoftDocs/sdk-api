---
UID: NN:wsdbase.IWSDUdpMessageParameters
title: IWSDUdpMessageParameters (wsdbase.h)
description: Use this interface to specify how often WSD repeats the message transmission.
helpviewer_keywords: ["IWSDUdpMessageParameters","IWSDUdpMessageParameters interface","IWSDUdpMessageParameters interface","described","ncd.iwsdudpmessageparameters","wsdbase/IWSDUdpMessageParameters"]
old-location: ncd\iwsdudpmessageparameters.htm
tech.root: ncd
ms.assetid: 3af6e0ff-c0b9-47af-b018-37567f614adc
ms.date: 12/05/2018
ms.keywords: IWSDUdpMessageParameters, IWSDUdpMessageParameters interface, IWSDUdpMessageParameters interface,described, ncd.iwsdudpmessageparameters, wsdbase/IWSDUdpMessageParameters
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
 - IWSDUdpMessageParameters
 - wsdbase/IWSDUdpMessageParameters
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
 - IWSDUdpMessageParameters
---

# IWSDUdpMessageParameters interface


## -description

Use this interface to specify how often WSD repeats the message transmission.

To get this interface from a UDP message sent during discovery, call the  <b>QueryInterface</b> method of <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a> passing __uuidof(IWSDUdpMessageParameters) as the interface identifier.

You can also call <a href="/windows/desktop/api/wsdbase/nf-wsdbase-wsdcreateudpmessageparameters">WSDCreateUdpMessageParameters</a> to retrieve this interface.

## -inheritance

The <b>IWSDUdpMessageParameters</b> interface inherits from <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>. <b>IWSDUdpMessageParameters</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>
