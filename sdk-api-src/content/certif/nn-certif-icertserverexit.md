---
UID: NN:certif.ICertServerExit
title: ICertServerExit
author: windows-sdk-content
description: Exported by the server engine and is called by exit modules.
old-location: security\icertserverexit.htm
old-project: SecCrypto
ms.assetid: 1554c09c-a7c1-44ad-9821-93c0913212fc
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: ICertServerExit, ICertServerExit interface [Security], ICertServerExit interface [Security],described, _certsrv_icertserverexit, certif/ICertServerExit, security.icertserverexit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certif.h
req.include-header: Certsrv.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerExit
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertServerExit interface


## -description


The <b>ICertServerExit</b> interface is exported by the server engine and is called by exit modules.

<b>ICertServerExit</b> allows exit modules to get and enumerate elements of requests and certificates.

<b>ICertServerExit</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerExit</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertServerExit</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertServerExit</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICertServerExit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385056(v=VS.85).aspx">EnumerateAttributes</a>
</td>
<td align="left" width="63%">
Returns the name of the next request attribute to be enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385057(v=VS.85).aspx">EnumerateAttributesClose</a>
</td>
<td align="left" width="63%">
Frees any resources connected with attribute enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385058(v=VS.85).aspx">EnumerateAttributesSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first attribute associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385061(v=VS.85).aspx">EnumerateExtensions</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) of the next certificate extension to be enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385064(v=VS.85).aspx">EnumerateExtensionsClose</a>
</td>
<td align="left" width="63%">
Frees any resources connected with extension enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385066(v=VS.85).aspx">EnumerateExtensionsSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first certificate extension associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385068(v=VS.85).aspx">GetCertificateExtension</a>
</td>
<td align="left" width="63%">
Gets a specified certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385072(v=VS.85).aspx">GetCertificateExtensionFlags</a>
</td>
<td align="left" width="63%">
Gets the flags from the extension acquired by the most recent call to 
<a href="https://msdn.microsoft.com/en-us/library/Aa385068(v=VS.85).aspx">GetCertificateExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385074(v=VS.85).aspx">GetCertificateProperty</a>
</td>
<td align="left" width="63%">
Returns a named certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385075(v=VS.85).aspx">GetRequestAttribute</a>
</td>
<td align="left" width="63%">
Returns a named request attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385077(v=VS.85).aspx">GetRequestProperty</a>
</td>
<td align="left" width="63%">
Returns a named request property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385079(v=VS.85).aspx">SetContext</a>
</td>
<td align="left" width="63%">
Sets the current instantiation of the interface to operate on the specified request context.

</td>
</tr>
</table> 

