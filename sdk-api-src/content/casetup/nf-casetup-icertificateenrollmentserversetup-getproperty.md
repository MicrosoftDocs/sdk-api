---
UID: NF:casetup.ICertificateEnrollmentServerSetup.GetProperty
title: ICertificateEnrollmentServerSetup::GetProperty (casetup.h)
description: Retrieves a CESSetupProperty enumeration value for the Certificate Enrollment Web Service (CES) configuration.
helpviewer_keywords: ["GetProperty","GetProperty method [Security]","GetProperty method [Security]","ICertificateEnrollmentServerSetup interface","ICertificateEnrollmentServerSetup interface [Security]","GetProperty method","ICertificateEnrollmentServerSetup.GetProperty","ICertificateEnrollmentServerSetup::GetProperty","casetup/ICertificateEnrollmentServerSetup::GetProperty","security.icertificateenrollmentserversetup_getproperty"]
old-location: security\icertificateenrollmentserversetup_getproperty.htm
tech.root: security
ms.assetid: 4B380551-742C-4D36-80C9-C92F62F916BB
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Security], GetProperty method [Security],ICertificateEnrollmentServerSetup interface, ICertificateEnrollmentServerSetup interface [Security],GetProperty method, ICertificateEnrollmentServerSetup.GetProperty, ICertificateEnrollmentServerSetup::GetProperty, casetup/ICertificateEnrollmentServerSetup::GetProperty, security.icertificateenrollmentserversetup_getproperty
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateEnrollmentServerSetup::GetProperty
 - casetup/ICertificateEnrollmentServerSetup::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentServerSetup.GetProperty
---

# ICertificateEnrollmentServerSetup::GetProperty


## -description

The <b>GetProperty</b> method retrieves a <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration value for the Certificate Enrollment Web Service (CES) configuration.

## -parameters

### -param propertyId [in]

A <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration value that specifies the property value to retrieve. For more information, see Remarks.

### -param pPropertyValue [out]

A pointer to a <b>VARIANT</b> variable that contains the property value.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>propertyId</i> argument is not a member of the <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPropertyValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a> object has not been initialized.

The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property value is set to "The setup object has not been initialized. Please initialize the setup object with the InitializeInstallDefaults method."

</td>
</tr>
</table>

## -remarks

The <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration type contains the following values:<ul>
<li><b>ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY</b></li>
<li><b>ENUM_CESSETUPPROP_CACONFIG</b></li>
<li><b>ENUM_CESSETUPPROP_AUTHENTICATION</b></li>
<li><b>ENUM_CESSETUPPROP_SSLCERTHASH</b></li>
<li><b>ENUM_CESSETUPPROP_URL</b></li>
<li><b>ENUM_CESSETUPPROP_RENEWALONLY</b></li>
</ul>


These values have the following meanings:

<ul>
<li>
The <b>ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY</b> property is a <b>VT_BOOL</b> value that specifies whether the server context is <b>ApplicationPoolIdentity</b>.

</li>
<li>
The <b>ENUM_CESSETUPPROP_CACONFIG</b> property contains a certification authority (CA) configuration string (<b>VT_BSTR</b>) of the form <i>computerDNSname</i>/<i>CAName</i> where <i>computerDNSname</i> is the fully qualified DNS name of the server and <i>CAName</i> is the common name of the CA.

</li>
<li>
The <b>ENUM_CESSETUPPROP_AUTHENTICATION</b> property specifies the type of authentication procedure used. If the  <b>GetProperty</b> method returns successfully, the <i>pPropertyValue</i> argument will contain one of the following constants: <ul>
<li>X509AuthKerberos</li>
<li>X509AuthUsername</li>
<li>X509AuthCertificate</li>
</ul>


</li>
<li>
The <b>ENUM_CESSETUPPROP_SSLCERTHASH</b> property contains the hash (<b>VT_BSTR</b>) of the certificate used during authentication. The <b>ENUM_CESSETUPPROP_AUTHENTICATION</b> property must be set to X509AuthCertificate.

</li>
<li>The <b>ENUM_CESSETUPPROP_URL</b> property contains the CES service URL. If the  <b>GetProperty</b> method returns successfully, the <i>pPropertyValue</i> argument will contain a <b>VT_BSTR</b> subtype that contains a URL of the form "https://<i>computerDNSname</i>/ADPolicyProvider_ces_<i>AuthenticationType</i>/service.svc/ces" where the authentication type can be one of the following:<ul>
<li>kerberos</li>
<li>usernamepassword</li>
<li>certificate</li>
</ul>
</li>
<li>The <b>ENUM_CESSETUPPROP_RENEWALONLY</b> property is a <b>VT_BOOL</b> value that specifies whether CES can process only certificate renewals.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>