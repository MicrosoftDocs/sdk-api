---
UID: NN:wsdattachment.IWSDInboundAttachment
title: IWSDInboundAttachment (wsdattachment.h)
description: Allows applications to read MIME-encoded attachment data from an incoming message.
helpviewer_keywords: ["IWSDInboundAttachment","IWSDInboundAttachment interface","IWSDInboundAttachment interface","described","ncd.iwsdinboundattachment","wsdattachment/IWSDInboundAttachment"]
old-location: ncd\iwsdinboundattachment.htm
tech.root: ncd
ms.assetid: 1bacbf20-2eb2-4aa1-ba37-e14dc0d955b0
ms.date: 12/05/2018
ms.keywords: IWSDInboundAttachment, IWSDInboundAttachment interface, IWSDInboundAttachment interface,described, ncd.iwsdinboundattachment, wsdattachment/IWSDInboundAttachment
req.header: wsdattachment.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdAttachment.idl
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
 - IWSDInboundAttachment
 - wsdattachment/IWSDInboundAttachment
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
 - IWSDInboundAttachment
---

# IWSDInboundAttachment interface


## -description

Allows applications to read MIME-encoded attachment data from an incoming message.

## -inheritance

The <b>IWSDInboundAttachment</b> interface inherits from <a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdattachment">IWSDAttachment</a>. <b>IWSDInboundAttachment</b> also has these types of members:

## -remarks

WSDAPI will provide an object implementing this interface when an attachment stream is received as part of a message.

## -see-also

<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdattachment">IWSDAttachment</a>
