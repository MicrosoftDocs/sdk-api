---
UID: NN:wsmandisp.IWSManConnectionOptionsEx2
title: IWSManConnectionOptionsEx2 (wsmandisp.h)

description: The IWSManConnectionOptionsEx2 object is passed to the IWSMan::CreateSession method to provide the authentication mechanism, access type, and credentials to connect to a proxy server.
old-location: winrm\iwsmanconnectionoptionsex2.htm
tech.root: winrm
ms.assetid: 09159904-0160-411d-af54-f6aca94d4d7d

ms.date: 12/05/2018
ms.keywords: IWSManConnectionOptionsEx2, IWSManConnectionOptionsEx2 interface [Windows Remote Management], IWSManConnectionOptionsEx2 interface [Windows Remote Management],described, winrm.iwsmanconnectionoptionsex2, wsmandisp/IWSManConnectionOptionsEx2
ms.topic: interface
f1_keywords: 
 - "wsmandisp/IWSManConnectionOptionsEx2"
dev_langs:
 - c++
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
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
 - WSManDisp.h
api_name:
 - IWSManConnectionOptionsEx2
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
---

# IWSManConnectionOptionsEx2 interface


## -description


The <b>IWSManConnectionOptionsEx2</b> object is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a> method to provide the authentication mechanism, access type, and credentials to connect to a proxy server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManConnectionOptionsEx2</b> interface inherits from <b>IWSManConnectionOptionsEx</b>. <b>IWSManConnectionOptionsEx2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSManConnectionOptionsEx2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-proxyauthenticationusebasic">ProxyAuthenticationUseBasic</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy authentication flag <b>WSManFlagProxyAuthenticationUseBasic</b> for use in the <i>authenticationMechanism</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-proxyauthenticationusedigest">ProxyAuthenticationUseDigest</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy authentication flag <b>WSManFlagProxyAuthenticationUseDigest</b> for use in the <i>authenticationMechanism</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-proxyauthenticationusenegotiate">ProxyAuthenticationUseNegotiate</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy authentication flag <b>WSManFlagProxyAuthenticationUseNegotiate</b> for use in the <i>authenticationMechanism</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-proxyautodetect">ProxyAutoDetect</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyAutoDetect</b> for use in the <i>accessType</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-proxyieconfig">ProxyIEConfig</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyIEConfig</b> for use in the <i>accessType</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-proxynoproxyserver">ProxyNoProxyServer</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyNoProxyServer</b> for use in the <i>accessType</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-proxywinhttpconfig">ProxyWinHttpConfig</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyWinHttpConfig</b> for use in the <i>accessType</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">SetProxy</a>
</td>
<td align="left" width="63%">
Sets the proxy information for the session.

</td>
</tr>
</table> 

