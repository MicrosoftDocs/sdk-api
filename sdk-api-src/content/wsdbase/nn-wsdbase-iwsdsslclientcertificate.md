---
UID: NN:wsdbase.IWSDSSLClientCertificate
title: IWSDSSLClientCertificate
author: windows-sdk-content
description: Retrieves the client SSL certificate.
old-location: ncd\iwsdsslclientcertificate.htm
old-project: wsdapi
ms.assetid: d1b5eb99-7bbb-4881-8251-4362368dff88
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: IWSDSSLClientCertificate, IWSDSSLClientCertificate interface, IWSDSSLClientCertificate interface,described, ncd.iwsdsslclientcertificate, wsdbase/IWSDSSLClientCertificate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDSSLClientCertificate
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDSSLClientCertificate interface


## -description


Retrieves the client SSL certificate.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDSSLClientCertificate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDSSLClientCertificate</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/82f3f4ae-80fe-4382-9a22-00c70e99524f">GetClientCertificate</a>
</td>
<td align="left" width="63%">
Gets the client certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79dbd838-cffd-4571-8227-e508673c1b02">GetMappedAccessToken</a>
</td>
<td align="left" width="63%">
Gets the mapped access token.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href=" http://go.microsoft.com/fwlink/p/?linkid=22407">QueryInterface</a> method of <a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a>.  If the connection did not arrive over SSL, the call to <a href=" http://go.microsoft.com/fwlink/p/?linkid=22407">QueryInterface</a> will return <b>E_NOINTERFACE</b>.

On the device host, the generated code calls the application's service method. This service method has access to the <a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a> interface through the <a href="https://msdn.microsoft.com/d8697474-bfe5-4704-b1ac-15cf96f2ca92">WSD_EVENT</a> structure. The <b>IWSDSSLClientCertificate</b> provides access to the client SSL certificate.



