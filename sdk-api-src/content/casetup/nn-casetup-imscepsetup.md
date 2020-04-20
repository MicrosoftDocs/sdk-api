---
UID: NN:casetup.IMSCEPSetup
title: IMSCEPSetup (casetup.h)
description: Defines functionality to install and uninstall a Network Device Enrollment Service (NDES) role on a Certificate Services computer.helpviewer_keywords: ["IMSCEPSetup","IMSCEPSetup interface [Security]","IMSCEPSetup interface [Security]","described","casetup/IMSCEPSetup","security.imscepsetup"]
old-location: security\imscepsetup.htm
tech.root: SecCrypto
ms.assetid: 328c6c04-7ade-4b64-bd8a-4314b6e8dc78
ms.date: 12/05/2018
ms.keywords: IMSCEPSetup, IMSCEPSetup interface [Security], IMSCEPSetup interface [Security],described, casetup/IMSCEPSetup, security.imscepsetup
f1_keywords:
- casetup/IMSCEPSetup
dev_langs:
- c++
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
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
- IMSCEPSetup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSCEPSetup interface


## -description


The <b>IMSCEPSetup</b> interface defines functionality to install and uninstall a Network Device Enrollment Service (NDES) role on a Certificate Services computer. Implement this interface to provide a custom setup program for installing and uninstalling this role.

Microsoft provides an implementation of this interface in the <b>CMSCEPSetup</b> class. For installation, you must call <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-initializedefaults">InitializeDefaults</a> before accessing any properties or calling any other methods on the <b>CMSCEPSetup</b> object.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CMSCEPSetup</b> class identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSCEPSetup</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMSCEPSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMSCEPSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-getkeylengthlist">GetKeyLengthList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key lengths</a> supported by the specified CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-getmscepsetupproperty">GetMSCEPSetupProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for an NDES configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-getprovidernamelist">GetProviderNameList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs) that provide asymmetric key signature and exchange algorithms on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-initializedefaults">InitializeDefaults</a>
</td>
<td align="left" width="63%">
Initializes a <b>CMSCEPSetup</b> object with default values to enable installation of an NDES role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-install">Install</a>
</td>
<td align="left" width="63%">
Installs an NDES role as configured in the <b>CMSCEPSetup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-ismscepstoreempty">IsMSCEPStoreEmpty</a>
</td>
<td align="left" width="63%">
This method always returns <b>VARIANT_TRUE</b>. It should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-postuninstall">PostUnInstall</a>
</td>
<td align="left" width="63%">
This method is not implemented. It is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-preuninstall">PreUnInstall</a>
</td>
<td align="left" width="63%">
Removes registry and IIS settings for the NDES role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-setaccountinformation">SetAccountInformation</a>
</td>
<td align="left" width="63%">
Sets the user account information used by the IIS NDES extension to perform enrollment on behalf of network devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-setmscepsetupproperty">SetMSCEPSetupProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for an NDES configuration.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSCEPSetup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-get_msceperrorid">MSCEPErrorId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ID for additional error information related to a failed NDES specification. Any method call on the parent object resets this property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-imscepsetup-get_msceperrorstring">MSCEPErrorString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the string data for additional error information related to a failed NDES specification. Any method call on the parent object resets this property.

</td>
</tr>
</table> 

