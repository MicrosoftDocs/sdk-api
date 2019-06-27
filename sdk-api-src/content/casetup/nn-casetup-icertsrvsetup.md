---
UID: NN:casetup.ICertSrvSetup
title: ICertSrvSetup (casetup.h)
author: windows-sdk-content
description: Defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a Certificate Services computer.
old-location: security\icertsrvsetup.htm
tech.root: SecCrypto
ms.assetid: 6792a0d6-d304-481d-a97b-5fb7033c7eae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup, ICertSrvSetup interface [Security], ICertSrvSetup interface [Security],described, casetup/ICertSrvSetup, security.icertsrvsetup
ms.topic: interface
f1_keywords: 
 - "casetup/ICertSrvSetup"
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertSrvSetup interface


## -description


The <b>ICertSrvSetup</b> interface defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Services</a> computer.

Microsoft provides an implementation of this interface in the <b>CCertSrvSetup</b> class. For installation, you must call the <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-initializedefaults">InitializeDefaults</a> method before accessing any properties or calling any other methods on the <b>CCertSrvSetup</b> object.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CCertSrvSetup</b> class identifier.

<b>Windows Server 2008 Standard:  </b>The following services are not available:<ul>
<li>Online Responder Service</li>
<li>Network Device Enrollment Service</li>
</ul>
In addition, the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) service has limited functionality:

<ul>
<li>V2 templates are not supported; therefore, autoenrollment is not supported.</li>
<li>Delegated enrollment agents are not supported.</li>
<li>Role separation is not supported.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetup</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertSrvSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertSrvSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-caimportpfx">CAImportPFX</a>
</td>
<td align="left" width="63%">
Imports a CA certificate and its associated <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> into the "LocalMachine" store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getcasetupproperty">GetCASetupProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for a CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getexistingcacertificates">GetExistingCACertificates</a>
</td>
<td align="left" width="63%">
Gets the collection of <b>CCertSrvSetupKeyInformation</b>  objects that represent valid CA certificates currently installed on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist">GetHashAlgorithmList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hashing algorithms</a> supported by the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) for an asymmetric key signature algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getkeylengthlist">GetKeyLengthList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key lengths</a> supported by the specified CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist">GetPrivateKeyContainerList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key container</a> names stored by the specified CSP for asymmetric key signature algorithms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getprovidernamelist">GetProviderNameList</a>
</td>
<td align="left" width="63%">
Gets the list of CSPs that provide asymmetric key signature algorithms on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getsupportedcatypes">GetSupportedCATypes</a>
</td>
<td align="left" width="63%">
Gets the types of CAs that can be installed on a computer under the caller context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-initializedefaults">InitializeDefaults</a>
</td>
<td align="left" width="63%">
Initializes a <b>CCertSrvSetup</b> object with default values to enable installation of a CA role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-install">Install</a>
</td>
<td align="left" width="63%">
Installs a CA role as configured in the <b>CCertSrvSetup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-ispropertyeditable">IsPropertyEditable</a>
</td>
<td align="left" width="63%">
Indicates to the caller whether a specified property can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-postuninstall">PostUnInstall</a>
</td>
<td align="left" width="63%">
This method is not implemented and is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-preuninstall">PreUnInstall</a>
</td>
<td align="left" width="63%">
Temporarily saves role-specific state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-setcadistinguishedname">SetCADistinguishedName</a>
</td>
<td align="left" width="63%">
Sets a CA common name and an optional distinguished name suffix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-setcasetupproperty">SetCASetupProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for a CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-setdatabaseinformation">SetDatabaseInformation</a>
</td>
<td align="left" width="63%">
Sets the database related information for the CA role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-setparentcainformation">SetParentCAInformation</a>
</td>
<td align="left" width="63%">
Sets the parent CA information for a subordinate CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-setwebcainformation">SetWebCAInformation</a>
</td>
<td align="left" width="63%">
Sets the CA information for the Certification Authority Web Enrollment role.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-get_caerrorid">CAErrorId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ID for additional error information related to a failed CA specification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-get_caerrorstring">CAErrorString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the string data for additional error information related to a failed CA specification.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

