---
UID: NN:wsdclient.IWSDAsyncCallback
title: IWSDAsyncCallback (wsdclient.h)
description: Handles callbacks for the completion of an asynchronous operation.
helpviewer_keywords: ["IWSDAsyncCallback","IWSDAsyncCallback interface","IWSDAsyncCallback interface","described","ncd.iwsdasynccallback","wsdclient/IWSDAsyncCallback"]
old-location: ncd\iwsdasynccallback.htm
tech.root: ncd
ms.assetid: 24108143-55b7-4098-a4cc-025dfdfd054a
ms.date: 12/05/2018
ms.keywords: IWSDAsyncCallback, IWSDAsyncCallback interface, IWSDAsyncCallback interface,described, ncd.iwsdasynccallback, wsdclient/IWSDAsyncCallback
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDAsyncCallback
 - wsdclient/IWSDAsyncCallback
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
 - IWSDAsyncCallback
---

# IWSDAsyncCallback interface


## -description

Handles callbacks for the completion of an asynchronous operation.

## -inheritance

The <b>IWSDAsyncCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDAsyncCallback</b> also has these types of members:

## -remarks

This interface provides an asynchronous calling pattern in support of WSDAPI messaging and eventing, allowing an application to receive callback notification based on the status of an operation.

The <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> interface can be used to wait for event notification or to poll for operation completion if asynchronous callbacks are not required.
