---
UID: NN:wsdbase.IWSDMessageParameters
title: IWSDMessageParameters (wsdbase.h)
description: Use this interface to communicate message specific information up and down the protocol stack.
helpviewer_keywords: ["IWSDMessageParameters","IWSDMessageParameters interface","IWSDMessageParameters interface","described","ncd.iwsdmessageparameters","wsdbase/IWSDMessageParameters"]
old-location: ncd\iwsdmessageparameters.htm
tech.root: ncd
ms.assetid: fb659a5e-1f55-47a6-b22d-660975d8c0fd
ms.date: 12/05/2018
ms.keywords: IWSDMessageParameters, IWSDMessageParameters interface, IWSDMessageParameters interface,described, ncd.iwsdmessageparameters, wsdbase/IWSDMessageParameters
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
 - IWSDMessageParameters
 - wsdbase/IWSDMessageParameters
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
 - IWSDMessageParameters
---

# IWSDMessageParameters interface


## -description

Use this interface to communicate message specific information up and down the protocol stack.

## -inheritance

The <b>IWSDMessageParameters</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDMessageParameters</b> also has these types of members:

## -remarks

In a request-response message pattern, the parameters also provide a way for the transport to determine where the response message for a given request should be sent. To enable this, the message parameters for a request must always be passed down the stack with the corresponding response.

Since message parameters can be packaged with a request or a response, and can be sent or received, the meaning of the local and remote address depends on the direction the message parameters.
