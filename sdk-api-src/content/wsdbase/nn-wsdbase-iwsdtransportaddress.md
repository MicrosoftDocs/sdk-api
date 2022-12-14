---
UID: NN:wsdbase.IWSDTransportAddress
title: IWSDTransportAddress (wsdbase.h)
description: Represents an IP-based transport address.
helpviewer_keywords: ["IWSDTransportAddress","IWSDTransportAddress interface","IWSDTransportAddress interface","described","ncd.iwsdtransportaddress","wsdbase/IWSDTransportAddress"]
old-location: ncd\iwsdtransportaddress.htm
tech.root: ncd
ms.assetid: 84dfee11-8092-4018-8840-e766a94c60a4
ms.date: 12/05/2018
ms.keywords: IWSDTransportAddress, IWSDTransportAddress interface, IWSDTransportAddress interface,described, ncd.iwsdtransportaddress, wsdbase/IWSDTransportAddress
req.header: wsdbase.h
req.include-header: Wsdapi.h
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
 - IWSDTransportAddress
 - wsdbase/IWSDTransportAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDTransportAddress
---

# IWSDTransportAddress interface


## -description

Represents an IP-based transport address.

You should not create an instance of the <b>IWSDTransportAddress</b> interface. Instead, create an instance of either the <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a> or <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a> interface if an address object is required.

## -inheritance

The <b>IWSDTransportAddress</b> interface inherits from <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a>. <b>IWSDTransportAddress</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a>
