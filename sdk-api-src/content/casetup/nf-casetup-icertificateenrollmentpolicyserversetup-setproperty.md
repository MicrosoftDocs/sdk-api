---
UID: NF:casetup.ICertificateEnrollmentPolicyServerSetup.SetProperty
title: ICertificateEnrollmentPolicyServerSetup::SetProperty (casetup.h)
description: Specifies a CEPSetupProperty enumeration value for the Certificate Enrollment Policy (CEP) Web Service configuration.
helpviewer_keywords: ["ICertificateEnrollmentPolicyServerSetup interface [Security]","SetProperty method","ICertificateEnrollmentPolicyServerSetup.SetProperty","ICertificateEnrollmentPolicyServerSetup::SetProperty","SetProperty","SetProperty method [Security]","SetProperty method [Security]","ICertificateEnrollmentPolicyServerSetup interface","casetup/ICertificateEnrollmentPolicyServerSetup::SetProperty","security.icertificateenrollmentpolicyserversetup_setproperty"]
old-location: security\icertificateenrollmentpolicyserversetup_setproperty.htm
tech.root: security
ms.assetid: 81E20BFF-B4EC-4FA5-A881-5BDCE3FC3057
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentPolicyServerSetup interface [Security],SetProperty method, ICertificateEnrollmentPolicyServerSetup.SetProperty, ICertificateEnrollmentPolicyServerSetup::SetProperty, SetProperty, SetProperty method [Security], SetProperty method [Security],ICertificateEnrollmentPolicyServerSetup interface, casetup/ICertificateEnrollmentPolicyServerSetup::SetProperty, security.icertificateenrollmentpolicyserversetup_setproperty
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
 - ICertificateEnrollmentPolicyServerSetup::SetProperty
 - casetup/ICertificateEnrollmentPolicyServerSetup::SetProperty
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
 - ICertificateEnrollmentPolicyServerSetup.SetProperty
---

# ICertificateEnrollmentPolicyServerSetup::SetProperty


## -description

The <b>SetProperty</b> method specifies a <a href="/windows/win32/api/casetup/ne-casetup-cepsetupproperty">CEPSetupProperty</a> enumeration value for the Certificate Enrollment Policy (CEP) Web Service configuration.

## -parameters

### -param propertyId [in]

A value of the <a href="/windows/win32/api/casetup/ne-casetup-cepsetupproperty">CEPSetupProperty</a> enumeration that specifies the property value to set. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>ENUM_CEPSETUPPROP_AUTHENTICATION</b></td>
<td>
The <i>pPropertyValue</i> parameter contains a value that identifies the type of authentication to be used.

</td>
</tr>
<tr>
<td><b>ENUM_CEPSETUPPROP_SSLCERTHASH</b></td>
<td>
The <i>pPropertyValue</i> parameter contains a hash of the certificate, if any, used during authentication. <b>ENUM_CEPSETUPPROP_AUTHENTICATION</b> must be set to X509AuthCertificate.

</td>
</tr>
<tr>
<td><b>ENUM_CEPSETUPPROP_KEYBASED_RENEWAL</b></td>
<td>
The <i>pPropertyValue</i> parameter specifies whether to set up the Enrollment Policy Server in a mode that returns policies for KeyBasedRenewal templates only.

</td>
</tr>
<tr>
<td><b>ENUM_CEPSETUPPROP_URL</b></td>
<td>
You cannot specify this  value.

</td>
</tr>
</table>

### -param pPropertyValue [in]

A pointer to a <b>VARIANT</b> variable that contains the property value.

If you specify <b>ENUM_CEPSETUPPROP_AUTHENTICATION</b> in the <i>propertyId</i> parameter, the  <b>VARIANT</b> subtype must be <b>VT_I2</b>, <b>VT_I4</b>  or <b>VT_UII4</b>, and the <i>pPropertyValue</i> argument must be one of the following constants: <ul>
<li><b>X509AuthKerberos</b></li>
<li><b>X509AuthUsername</b></li>
<li><b>X509AuthCertificate</b></li>
</ul>


If you specify <b>ENUM_CEPSETUPPROP_SSLCERTHASH</b> in the <i>propertyId</i> parameter, you must set the <i>pPropertyValue</i> parameter to a <b>VT_BSTR</b> subtype that contains a hash of the certificate used for authentication.

If you specify <b>ENUM_CEPSETUPPROP_AUTHENTICATION</b> in the <i>propertyId</i> parameter, the <i>pPropertyValue</i> parameter contains the authentication procedure.

If you specify <b>ENUM_CEPSETUPPROP_URL</b> in the <i>propertyId</i> parameter, the <i>pPropertyValue</i> parameter contains the Certificate Enrollment Policy (CEP) Web Service URL.

If you specify <b>ENUM_CEPSETUPPROP_KEYBASED_RENEWAL</b> in the <i>propertyId</i> parameter, you must set the <i>pPropertyValue</i> parameter to the <b>VT_BOOL</b> subtype that indicates  whether to set up the Enrollment Policy Server in a mode that returns policies for KeyBasedRenewal templates only.

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
The <i>propertyId</i> argument is not a member of the <a href="/windows/win32/api/casetup/ne-casetup-cepsetupproperty">CEPSetupProperty</a> enumeration type or you have tried to set the <b>ENUM_CEPSETUPPROP_URL</b> value.

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
The <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> object has not been initialized.

The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-get_errorstring">ErrorString</a> property value is set to "The setup object has not been initialized. Please initialize the setup object with the InitializeInstallDefaults method."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH)</b></dt>
</dl>
</td>
<td width="60%">
If you are setting the <b>ENUM_CEPSETUPPROP_AUTHENTICATION</b> property, the <b>VARIANT</b> subtype must be <b>VT_I2</b>, <b>VT_I4</b>, or <b>VT_UI4</b>.

</td>
</tr>
</table>

## -remarks

You must call <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-initializeinstalldefaults">InitializeInstallDefaults</a> before calling the <b>SetProperty</b> method.

## -see-also

<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-getproperty">GetProperty</a>



<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a>



<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-initializeinstalldefaults">InitializeInstallDefaults</a>