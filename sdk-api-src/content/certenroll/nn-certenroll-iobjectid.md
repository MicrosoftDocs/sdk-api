---
UID: NN:certenroll.IObjectId
title: IObjectId
author: windows-sdk-content
description: Represents an object identifier (OID).
old-location: security\iobjectid.htm
old-project: seccertenroll
ms.assetid: bc6608e3-cae7-4992-b599-06bc04cc8ad7
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IObjectId, IObjectId interface [Security], IObjectId interface [Security],described, certenroll/IObjectId, security.iobjectid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CertEnroll.dll
api_name:
 - IObjectId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IObjectId interface


## -description


The <b>IObjectId</b> interface represents an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID). OIDs are returned from numerous Certificate Enrollment API properties, and they  can be used to initialize the following objects:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa374981(v=VS.85).aspx">IAlternativeName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375225(v=VS.85).aspx">ICertificatePolicy</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377059(v=VS.85).aspx">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378132(v=VS.85).aspx">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
</li>
</ul>


All of the methods used to initialize an <b>IObjectId</b> object call the CryptoAPI <a href="https://msdn.microsoft.com/en-us/library/Aa379938(v=VS.85).aspx">CryptFindOIDInfo</a> function which retrieves the first registered <a href="https://msdn.microsoft.com/en-us/library/Aa381435(v=VS.85).aspx">CRYPT_OID_INFO</a> structure that matches the specified parameters. The function searches the registry and static memory on the local computer and Active Directory on the domain server. The  <b>CRYPT_OID_INFO</b> structure is declared in Wincrypt.h and has the following signature.<div class="alert"><b>Note</b>  You cannot use the <a href="https://msdn.microsoft.com/en-us/library/Aa381435(v=VS.85).aspx">CRYPT_OID_INFO</a> structure directly in the Certificate Enrollment API.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectId</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IObjectId</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IObjectId</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa965697(v=VS.85).aspx">GetAlgorithmName</a>
</td>
<td align="left" width="63%">
Retrieves the display name associated with an algorithm object identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376796(v=VS.85).aspx">InitializeFromAlgorithmName</a>
</td>
<td align="left" width="63%">
Initializes the object from an algorithm name or an object identifier.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376797(v=VS.85).aspx">InitializeFromName</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a> enumeration value.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376798(v=VS.85).aspx">InitializeFromValue</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains a dotted decimal object identifier.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectId</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376795(v=VS.85).aspx">FriendlyName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies and retrieves a display name for the object identifier.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBECTID</a> value that contains an object identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Hh449625(v=VS.85).aspx">Value</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a string that contains the dotted decimal object identifier.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a>
 

 

