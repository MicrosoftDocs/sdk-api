---
UID: NF:casetup.ICertificateEnrollmentServerSetup.SetProperty
title: ICertificateEnrollmentServerSetup::SetProperty (casetup.h)
description: Specifies a CESSetupProperty enumeration value for the Certificate Enrollment Web Service (CES) configuration.
helpviewer_keywords: ["ICertificateEnrollmentServerSetup interface [Security]","SetProperty method","ICertificateEnrollmentServerSetup.SetProperty","ICertificateEnrollmentServerSetup::SetProperty","SetProperty","SetProperty method [Security]","SetProperty method [Security]","ICertificateEnrollmentServerSetup interface","casetup/ICertificateEnrollmentServerSetup::SetProperty","security.icertificateenrollmentserversetup_setproperty"]
old-location: security\icertificateenrollmentserversetup_setproperty.htm
tech.root: security
ms.assetid: D2E20195-D81F-4717-83D2-BF8DC1D1779B
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentServerSetup interface [Security],SetProperty method, ICertificateEnrollmentServerSetup.SetProperty, ICertificateEnrollmentServerSetup::SetProperty, SetProperty, SetProperty method [Security], SetProperty method [Security],ICertificateEnrollmentServerSetup interface, casetup/ICertificateEnrollmentServerSetup::SetProperty, security.icertificateenrollmentserversetup_setproperty
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
 - ICertificateEnrollmentServerSetup::SetProperty
 - casetup/ICertificateEnrollmentServerSetup::SetProperty
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
 - ICertificateEnrollmentServerSetup.SetProperty
---

# ICertificateEnrollmentServerSetup::SetProperty


## -description

The <b>SetProperty</b> method specifies a <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration value for the Certificate Enrollment Web Service (CES) configuration.

## -parameters

### -param propertyId [in]

A <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration value that specifies the property value to retrieve.

### -param pPropertyValue [in]

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

Also, if you are setting the <b>ENUM_CESSETUPPROP_AUTHENTICATION</b> property, you must specify one of the following values in the <i>pPropertyValue</i> argument:<ul>
<li><b>X509AuthKerberos</b></li>
<li><b>X509AuthUsername</b></li>
<li><b>X509AuthCertificate</b></li>
</ul>


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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH)</b></dt>
</dl>
</td>
<td width="60%">
If you are setting the <b>ENUM_CESSETUPPROP_AUTHENTICATION</b> property, the <b>VARIANT</b> subtype must be <b>VT_I2</b>, <b>VT_I4</b>, or <b>VT_UI4</b>.

</td>
</tr>
</table>

## -remarks

You must call  <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-initializeinstalldefaults">InitializeInstallDefaults</a> before calling <b>SetProperty</b>.

You cannot set the <b>ENUM_CESSETUPPROP_URL</b> property.

You cannot set the <b>ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY</b> if the WSEnrollmentServer application pool already exists and WMI has been initialized.

If you are setting the <b>ENUM_CESSETUPPROP_AUTHENTICATION</b> property, the  <b>VARIANT</b> subtype must be <b>VT_I2</b>, <b>VT_I4</b>  or <b>VT_UII4</b>, and the <i>pPropertyValue</i> argument must be one of the following constants: <ul>
<li><b>X509AuthKerberos</b></li>
<li><b>X509AuthUsername</b></li>
<li><b>X509AuthCertificate</b></li>
</ul>


You cannot set the ENUM_CESSETUPPROP_CACONFIG property if the target server is a standalone certification authority. The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property will be set to "The Certificate Enrollment Web Service cannot be used with a standalone certification authority (CA). It can only be used with an enterprise CA."

.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>