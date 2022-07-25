---
UID: NN:wsdbase.IWSDSSLClientCertificate
title: IWSDSSLClientCertificate (wsdbase.h)
description: Retrieves the client SSL certificate.
helpviewer_keywords: ["IWSDSSLClientCertificate","IWSDSSLClientCertificate interface","IWSDSSLClientCertificate interface","described","ncd.iwsdsslclientcertificate","wsdbase/IWSDSSLClientCertificate"]
old-location: ncd\iwsdsslclientcertificate.htm
tech.root: ncd
ms.assetid: d1b5eb99-7bbb-4881-8251-4362368dff88
ms.date: 12/05/2018
ms.keywords: IWSDSSLClientCertificate, IWSDSSLClientCertificate interface, IWSDSSLClientCertificate interface,described, ncd.iwsdsslclientcertificate, wsdbase/IWSDSSLClientCertificate
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IWSDSSLClientCertificate
 - wsdbase/IWSDSSLClientCertificate
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
 - IWSDSSLClientCertificate
---

# IWSDSSLClientCertificate interface


## -description

Retrieves the client SSL certificate.

## -inheritance

The <b>IWSDSSLClientCertificate</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDSSLClientCertificate</b> also has these types of members:

## -remarks

An application can acquire this interface by calling the <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>.  If the connection did not arrive over SSL, the call to <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> will return <b>E_NOINTERFACE</b>.

On the device host, the generated code calls the application's service method. This service method has access to the <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a> interface through the <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_event">WSD_EVENT</a> structure. The <b>IWSDSSLClientCertificate</b> provides access to the client SSL certificate.
