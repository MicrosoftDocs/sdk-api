---
UID: NN:certenroll.IObjectId
title: IObjectId (certenroll.h)
author: windows-sdk-content
description: Represents an object identifier (OID).
old-location: security\iobjectid.htm
tech.root: seccertenroll
ms.assetid: bc6608e3-cae7-4992-b599-06bc04cc8ad7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IObjectId, IObjectId interface [Security], IObjectId interface [Security],described, certenroll/IObjectId, security.iobjectid
ms.topic: interface
f1_keywords: 
 - "certenroll/IObjectId"
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectId interface


## -description


The <b>IObjectId</b> interface represents an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). OIDs are returned from numerous Certificate Enrollment API properties, and they  can be used to initialize the following objects:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>
</li>
</ul>


All of the methods used to initialize an <b>IObjectId</b> object call the CryptoAPI <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function which retrieves the first registered <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crypt_oid_info">CRYPT_OID_INFO</a> structure that matches the specified parameters. The function searches the registry and static memory on the local computer and Active Directory on the domain server. The  <b>CRYPT_OID_INFO</b> structure is declared in Wincrypt.h and has the following signature.<div class="alert"><b>Note</b>  You cannot use the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crypt_oid_info">CRYPT_OID_INFO</a> structure directly in the Certificate Enrollment API.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectId</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IObjectId</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-getalgorithmname">GetAlgorithmName</a>
</td>
<td align="left" width="63%">
Retrieves the display name associated with an algorithm object identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a>
</td>
<td align="left" width="63%">
Initializes the object from an algorithm name or an object identifier.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromname">InitializeFromName</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a> enumeration value.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromvalue">InitializeFromValue</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_friendlyname">FriendlyName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_name">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBECTID</a> value that contains an object identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_value">Value</a>


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




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>
 

 

