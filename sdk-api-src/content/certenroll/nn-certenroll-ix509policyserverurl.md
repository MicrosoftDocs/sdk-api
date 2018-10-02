---
UID: NN:certenroll.IX509PolicyServerUrl
title: IX509PolicyServerUrl
author: windows-sdk-content
description: The IX509PolicyServerUrl interface can be used to set or retrieve property values associated with the certificate enrollment policy (CEP) server and to update associated registry values.
old-location: security\ix509policyserverurl.htm
tech.root: SecCertEnroll
ms.assetid: ad9d61ec-f607-4f71-ad8a-28d821e29c27
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509PolicyServerUrl, IX509PolicyServerUrl interface [Security], IX509PolicyServerUrl interface [Security],described, certenroll/IX509PolicyServerUrl, security.ix509policyserverurl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
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
req.type-library: CertEnroll.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PolicyServerUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PolicyServerUrl interface


## -description


The <b>IX509PolicyServerUrl</b> interface can be used to set or retrieve property values associated with the certificate enrollment policy (CEP) server and to update associated registry values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509PolicyServerUrl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509PolicyServerUrl</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509PolicyServerUrl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351739(v=VS.85).aspx">GetStringProperty</a>
</td>
<td align="left" width="63%">
Retrieves the CEP server ID or the display name of the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351740(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509PolicyServerUrl</b> object for a computer or user context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351741(v=VS.85).aspx">RemoveFromRegistry</a>
</td>
<td align="left" width="63%">
Unregisters a CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351742(v=VS.85).aspx">SetStringProperty</a>
</td>
<td align="left" width="63%">
Specifies the CEP server ID or the display name of the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351743(v=VS.85).aspx">UpdateRegistry</a>
</td>
<td align="left" width="63%">
Registers a CEP server.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509PolicyServerUrl</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351735(v=VS.85).aspx">AuthFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies and retrieves a value that indicates the authentication type used by the client to authenticate itself to the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351736(v=VS.85).aspx">Cost</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies and retrieves an arbitrary  cost for contacting the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351737(v=VS.85).aspx">Default</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that indicates whether this is the default CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351738(v=VS.85).aspx">Flags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates whether the CEP server policy information can be loaded from group policy, from the registry, or both.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351744(v=VS.85).aspx">Url</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the URL for the certificate enrollment policy (CEP) server.

</td>
</tr>
</table> 

