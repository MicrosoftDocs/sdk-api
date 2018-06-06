---
UID: NN:wsmandisp.IWSManConnectionOptionsEx2
title: IWSManConnectionOptionsEx2
author: windows-sdk-content
description: The IWSManConnectionOptionsEx2 object is passed to the IWSMan::CreateSession method to provide the authentication mechanism, access type, and credentials to connect to a proxy server.
old-location: winrm\iwsmanconnectionoptionsex2.htm
old-project: WinRM
ms.assetid: 09159904-0160-411d-af54-f6aca94d4d7d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSManConnectionOptionsEx2, IWSManConnectionOptionsEx2 interface [Windows Remote Management], IWSManConnectionOptionsEx2 interface [Windows Remote Management],described, winrm.iwsmanconnectionoptionsex2, wsmandisp/IWSManConnectionOptionsEx2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSManDisp.h
api_name:
 - IWSManConnectionOptionsEx2
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManConnectionOptionsEx2 interface


## -description


The <b>IWSManConnectionOptionsEx2</b> object is passed to the <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a> method to provide the authentication mechanism, access type, and credentials to connect to a proxy server.


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
<a href="https://msdn.microsoft.com/4bfce6f5-9980-4158-be1d-0f3ec081a9b2">ProxyAuthenticationUseBasic</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy authentication flag <b>WSManFlagProxyAuthenticationUseBasic</b> for use in the <i>authenticationMechanism</i> parameter of the <a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6813d121-2f02-4678-80fc-161dcb1d78ea">ProxyAuthenticationUseDigest</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy authentication flag <b>WSManFlagProxyAuthenticationUseDigest</b> for use in the <i>authenticationMechanism</i> parameter of the <a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7dfed5c-7897-4289-bd69-5f6fffaf66f7">ProxyAuthenticationUseNegotiate</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy authentication flag <b>WSManFlagProxyAuthenticationUseNegotiate</b> for use in the <i>authenticationMechanism</i> parameter of the <a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c277ce3-2655-4efc-abb4-224c28531d97">ProxyAutoDetect</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyAutoDetect</b> for use in the <i>accessType</i> parameter of the <a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4aa2bf90-c0e8-400a-a8c7-35656cb3c021">ProxyIEConfig</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyIEConfig</b> for use in the <i>accessType</i> parameter of the <a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00613052-7428-4719-9a19-fc27541af07a">ProxyNoProxyServer</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyNoProxyServer</b> for use in the <i>accessType</i> parameter of the <a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a44cd693-cf85-4c04-89d5-920e4c2972a4">ProxyWinHttpConfig</a>
</td>
<td align="left" width="63%">
Returns the value of the proxy access type flag <b>WSManProxyWinHttpConfig</b> for use in the <i>accessType</i> parameter of the <a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b87d5625-c77d-41cb-a75d-a45ba0d3fbe6">SetProxy</a>
</td>
<td align="left" width="63%">
Sets the proxy information for the session.

</td>
</tr>
</table> 

