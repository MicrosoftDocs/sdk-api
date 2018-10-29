---
UID: NN:mfidl.IMFSSLCertificateManager
title: IMFSSLCertificateManager
author: windows-sdk-content
description: Implemented by a client and called by Microsoft Media Foundation to get the client Secure Sockets Layer (SSL) certificate requested by the server.
old-location: mf\imfsslcertificatemanager.htm
tech.root: medfound
ms.assetid: 62e4227d-6bc9-4011-acee-6278fe388830
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFSSLCertificateManager, IMFSSLCertificateManager interface [Media Foundation], IMFSSLCertificateManager interface [Media Foundation],described, mf.imfsslcertificatemanager, mfidl/IMFSSLCertificateManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSSLCertificateManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSSLCertificateManager interface


## -description


Implemented by a client and called by Microsoft Media Foundation to get the client Secure Sockets Layer (SSL) certificate requested by the server. 

In most HTTPS connections the server provides a certificate so that the client can ensure the identity of the server. However, in certain cases the server might wants to verify the identity of the client by requesting the client to send a certificate. For this scenario,  a client application must provide a mechanism for Media Foundation to retrieve the client side certificate while opening an HTTPS URL with the source resolver or the scheme handler. The application must implement <b>IMFSSLCertificateManager</b>, set the <b>IUnknown</b> pointer of the implemented object in the <a href="https://msdn.microsoft.com/13e05bda-96c2-4095-a266-74185760f33a">MFNETSOURCE_SSLCERTIFICATE_MANAGER</a> property, and pass the property store to the source resolver. While opening the URL, Media Foundation calls the <b>IMFSSLCertificateManager</b> methods to get the certificate information. If the application needs to connect to HTTPS URL that requires a client-side certificate, or the application  wants customized control over the type of server certificates to accept, then they can implement this interface. This interface can also be used by the application to validate the server SSL certificate.

If the <b>IUnknown</b> pointer is not provided by the application and the HTTPS URL does not require the client to provide a certificate,
Media Foundation uses the default implementation to open the URL.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSSLCertificateManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSSLCertificateManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSSLCertificateManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e375cb97-bb43-4852-9671-dd8fdea34cef">BeginGetClientCertificate</a>
</td>
<td align="left" width="63%">
Starts an asynchronous call to get the client SSL certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25cd2ab0-7f58-4bd5-b594-75a3acbdc2d9">EndGetClientCertificate</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to get the client SSL certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/343f86ca-0036-4324-b3ca-4dba8fbc26a8">GetCertificatePolicy</a>
</td>
<td align="left" width="63%">
Indicates whether the server SSL certificate must be verified by the caller, MF,  or the <b>IMFSSLCertificateManager</b> implementation class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11a575e8-5eb2-4cbb-a460-f1ea5d54d324">GetClientCertificate</a>
</td>
<td align="left" width="63%">
Gets the client SSL certificate synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ba43175-4429-437d-acfb-e0ea8d300651">OnServerCertificate</a>
</td>
<td align="left" width="63%">
Indicates whether the server SSL certificate is accepted.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

