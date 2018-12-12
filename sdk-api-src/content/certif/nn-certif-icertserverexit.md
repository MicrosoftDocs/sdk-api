---
UID: NN:certif.ICertServerExit
title: ICertServerExit
author: windows-sdk-content
description: Exported by the server engine and is called by exit modules.
old-location: security\icertserverexit.htm
tech.root: seccrypto
ms.assetid: 1554c09c-a7c1-44ad-9821-93c0913212fc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertServerExit, ICertServerExit interface [Security], ICertServerExit interface [Security],described, _certsrv_icertserverexit, certif/ICertServerExit, security.icertserverexit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certif.h
req.include-header: Certsrv.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ICertServerExit interface


## -description


The <b>ICertServerExit</b> interface is exported by the server engine and is called by exit modules.

<b>ICertServerExit</b> allows exit modules to get and enumerate elements of requests and certificates.

<b>ICertServerExit</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerExit</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertServerExit</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertServerExit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/df778207-3b20-45a5-a705-8dba566eb658">EnumerateAttributes</a>
</td>
<td align="left" width="63%">
Returns the name of the next request attribute to be enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ac7afbb-49c6-45b3-a27e-5ba995684848">EnumerateAttributesClose</a>
</td>
<td align="left" width="63%">
Frees any resources connected with attribute enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c81b9c4d-483e-48b8-a270-f570e148d371">EnumerateAttributesSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first attribute associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8726f5fa-dc85-4357-b73a-013842d6ab78">EnumerateExtensions</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the next certificate extension to be enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/769235cd-d5ef-458b-a04b-88f9f831ce3f">EnumerateExtensionsClose</a>
</td>
<td align="left" width="63%">
Frees any resources connected with extension enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a0c4919-b3a0-4027-85bd-970f6bc0cdeb">EnumerateExtensionsSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first certificate extension associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba2d2e5f-230e-4e69-8d86-dad9c743e5ee">GetCertificateExtension</a>
</td>
<td align="left" width="63%">
Gets a specified certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0eee1d67-116b-4f93-9273-b70d50fa2c5d">GetCertificateExtensionFlags</a>
</td>
<td align="left" width="63%">
Gets the flags from the extension acquired by the most recent call to 
<a href="https://msdn.microsoft.com/ba2d2e5f-230e-4e69-8d86-dad9c743e5ee">GetCertificateExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a6185cd-fae5-4ee6-b403-c7613b31e48a">GetCertificateProperty</a>
</td>
<td align="left" width="63%">
Returns a named certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/894bde77-5e76-452b-acf5-c73fcaf1fa31">GetRequestAttribute</a>
</td>
<td align="left" width="63%">
Returns a named request attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9b98573-4eb0-4add-988b-dc34d6c15436">GetRequestProperty</a>
</td>
<td align="left" width="63%">
Returns a named request property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d317114-17bd-4b22-8e37-99db72740538">SetContext</a>
</td>
<td align="left" width="63%">
Sets the current instantiation of the interface to operate on the specified request context.

</td>
</tr>
</table> 

