---
UID: NN:certenroll.ICspInformation
title: ICspInformation (certenroll.h)
description: Provides access to general information about a cryptographic provider.
old-location: security\icspinformation.htm
tech.root: seccertenroll
ms.assetid: e337ae2c-6f86-4025-8d31-47bc5d8a4ca8
ms.date: 12/05/2018
ms.keywords: ICspInformation, ICspInformation interface [Security], ICspInformation interface [Security],described, certenroll/ICspInformation, security.icspinformation
ms.topic: interface
f1_keywords:
- certenroll/ICspInformation
dev_langs:
- c++
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
- ICspInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspInformation interface


## -description


The <b>ICspInformation</b> interface provides access to general information about a cryptographic  provider. The information is initialized by calling the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromname">InitializeFromName</a> or <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromtype">InitializeFromType</a> method. The information is retrieved by using the following methods and properties. For information about CSPs, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/csps-and-the-cryptography-process">CSPs and the Cryptography Process</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformation</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICspInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-getcspstatusfromoperations">GetCspStatusFromOperations</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object for the first supported algorithm that is consistent with the specified signature, encryption, hashing, or cipher  operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-getdefaultsecuritydescriptor">GetDefaultSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the default private key security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromname">InitializeFromName</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains a provider name.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromtype">InitializeFromType</a>
</td>
<td align="left" width="63%">
Initializes the object from the default cryptographic provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformation</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_cspalgorithms">CspAlgorithms</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a> interfaces that contain information about the algorithms supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_hashardwarerandomnumbergenerator">HasHardwareRandomNumberGenerator</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider supports a hardware random number generator that can be used to create random bytes for cryptographic operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_ishardwaredevice">IsHardwareDevice</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that determines whether the provider is implemented in a hardware device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_isremovable">IsRemovable</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the token that contains the key can be removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issmartcard">IsSmartCard</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is a smart card provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issoftwaredevice">IsSoftwareDevice</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is implemented in software.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_keyspec">KeySpec</a>


</td>
<td align="left" width="63%">
Retrieves a value that specifies the intended use of the algorithms supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_legacycsp">LegacyCsp</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is a Cryptography API: Next Generation (CNG) provider or a CryptoAPI (legacy) CSP.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_maxkeycontainernamelength">MaxKeyContainerNameLength</a>


</td>
<td align="left" width="63%">
Retrieves the maximum supported length for the name of the private key container associated with the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_name">Name</a>


</td>
<td align="left" width="63%">
Retrieves the name of the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_type">Type</a>


</td>
<td align="left" width="63%">
Retrieves the type of the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_valid">Valid</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is installed on the client computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_version">Version</a>


</td>
<td align="left" width="63%">
Retrieves the version number of the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

