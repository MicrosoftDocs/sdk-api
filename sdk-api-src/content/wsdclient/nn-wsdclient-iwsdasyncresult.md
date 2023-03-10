---
UID: NN:wsdclient.IWSDAsyncResult
title: IWSDAsyncResult (wsdclient.h)
description: Represents an asynchronous operation.
helpviewer_keywords: ["IWSDAsyncResult","IWSDAsyncResult interface","IWSDAsyncResult interface","described","ncd.iwsdasyncresult","wsdclient/IWSDAsyncResult"]
old-location: ncd\iwsdasyncresult.htm
tech.root: ncd
ms.assetid: 49c5ad02-f24b-4ef9-b943-483728c0bbcd
ms.date: 12/05/2018
ms.keywords: IWSDAsyncResult, IWSDAsyncResult interface, IWSDAsyncResult interface,described, ncd.iwsdasyncresult, wsdclient/IWSDAsyncResult
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
 - IWSDAsyncResult
 - wsdclient/IWSDAsyncResult
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
 - IWSDAsyncResult
---

# IWSDAsyncResult interface


## -description

Represents an asynchronous operation.

## -inheritance

The <b>IWSDAsyncResult</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDAsyncResult</b> also has these types of members:

## -remarks

The <b>IWSDAsyncResult</b> interface can be used to set a wait handle to receive event or message notification or poll for operation completion. It can also retrieve the state of an asynchronous operation and retrieve the results and response body of the event.

The <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> interface can be used to provide an asynchronous calling pattern in support of WSDAPI messaging and eventing, allowing an application to receive callback notification based on the status of an operation.



A failed asynchronous operation is treated as a completed asynchronous operation. Error or fault information can be retrieved from the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> interface using the <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasynccallback-asyncoperationcomplete">IWSDAsyncCallback::AsyncOperationComplete</a> method.
