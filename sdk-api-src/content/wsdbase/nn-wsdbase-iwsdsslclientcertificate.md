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
f1_keywords:
- wsdbase/IWSDSSLClientCertificate
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wsdapi.dll
api_name:
- IWSDSSLClientCertificate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDSSLClientCertificate interface


## -description


Retrieves the client SSL certificate.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDSSLClientCertificate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDSSLClientCertificate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDSSLClientCertificate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdsslclientcertificate-getclientcertificate">GetClientCertificate</a>
</td>
<td align="left" width="63%">
Gets the client certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdsslclientcertificate-getmappedaccesstoken">GetMappedAccessToken</a>
</td>
<td align="left" width="63%">
Gets the mapped access token.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://msdn2.microsoft.com/library/ms682521.aspx">QueryInterface</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>.  If the connection did not arrive over SSL, the call to <a href="https://msdn2.microsoft.com/library/ms682521.aspx">QueryInterface</a> will return <b>E_NOINTERFACE</b>.

On the device host, the generated code calls the application's service method. This service method has access to the <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a> interface through the <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_event">WSD_EVENT</a> structure. The <b>IWSDSSLClientCertificate</b> provides access to the client SSL certificate.



