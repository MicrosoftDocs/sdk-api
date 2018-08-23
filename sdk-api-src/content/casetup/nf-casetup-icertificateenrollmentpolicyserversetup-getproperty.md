---
UID: NF:casetup.ICertificateEnrollmentPolicyServerSetup.GetProperty
title: ICertificateEnrollmentPolicyServerSetup::GetProperty
author: windows-sdk-content
description: Retrieves a CEPSetupProperty enumeration value for the Certificate Enrollment Policy (CEP) Web Service configuration.
old-location: security\icertificateenrollmentpolicyserversetup_getproperty.htm
old-project: SecCrypto
ms.assetid: 52AD50BB-4146-44FC-BA32-9FC46FFE32E4
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetProperty, GetProperty method [Security], GetProperty method [Security],ICertificateEnrollmentPolicyServerSetup interface, ICertificateEnrollmentPolicyServerSetup interface [Security],GetProperty method, ICertificateEnrollmentPolicyServerSetup.GetProperty, ICertificateEnrollmentPolicyServerSetup::GetProperty, casetup/ICertificateEnrollmentPolicyServerSetup::GetProperty, security.icertificateenrollmentpolicyserversetup_getproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: casetup.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CEPSetupProperty
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentPolicyServerSetup.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertificateEnrollmentPolicyServerSetup::GetProperty


## -description


The <b>GetProperty</b> method retrieves a <a href="https://msdn.microsoft.com/en-us/library/Ff808352(v=VS.85).aspx">CEPSetupProperty</a> enumeration value for the Certificate Enrollment Policy (CEP) Web Service configuration.


## -parameters




### -param propertyId [in]

A value of the <a href="https://msdn.microsoft.com/en-us/library/Ff808352(v=VS.85).aspx">CEPSetupProperty</a> enumeration that specifies the property value to set. The following values are valid.

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
The <i>pPropertyValue</i> parameter contains a hash of the certificate, if any, used during authentication.

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
Contains the CEP service URL. If the  <b>GetProperty</b> method returns successfully, the <i>pPropertyValue</i> argument will contain a <b>VT_BSTR</b> subtype that contains a URL of the form "https://<i>computerDNSname</i>/ADPolicyProvider_cep_<i>AuthenticationType</i>/service.svc/cep" where the authentication type can be one of the following:<ul>
<li>kerberos</li>
<li>usernamepassword</li>
<li>certificate</li>
</ul>


</td>
</tr>
</table>
 


### -param pPropertyValue [out]

A pointer to a <b>VARIANT</b> variable that contains the property value.

If you specify <b>ENUM_CEPSETUPPROP_AUTHENTICATION</b> in the <i>propertyId</i> parameter, the <i>pPropertyValue</i> parameter will contain one of the following constants if the  <b>GetProperty</b> method returns successfully: <ul>
<li><b>X509AuthKerberos</b></li>
<li><b>X509AuthUsername</b></li>
<li><b>X509AuthCertificate</b></li>
</ul>


If you specify <b>ENUM_CEPSETUPPROP_SSLCERTHASH</b> in the <i>propertyId</i> parameter, the <i>pPropertyValue</i> parameter will contain a <b>VT_BSTR</b> subtype that contains the hash if the  <b>GetProperty</b> method returns successfully.

If you specify <b>ENUM_CEPSETUPPROP_AUTHENTICATION</b> in the <i>propertyId</i> parameter, the <i>pPropertyValue</i> parameter contains the authentication procedure.

If you specify <b>ENUM_CEPSETUPPROP_URL</b> in the <i>propertyId</i> parameter, the <i>pPropertyValue</i> parameter contains the Certificate Enrollment Policy (CEP) Web Service URL.

If you specify <b>ENUM_CEPSETUPPROP_KEYBASED_RENEWAL</b> in the <i>propertyId</i> parameter, you must set the <i>pPropertyValue</i> parameter to the <b>VT_BOOL</b> subtype that  indicates  whether to set up the Enrollment Policy Server in a mode that returns policies for KeyBasedRenewal templates only.


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
The <i>propertyId</i> argument is not a member of the <a href="https://msdn.microsoft.com/en-us/library/Ff808352(v=VS.85).aspx">CEPSetupProperty</a> enumeration type.

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
The <a href="https://msdn.microsoft.com/en-us/library/Ff808370(v=VS.85).aspx">ICertificateEnrollmentPolicyServerSetup</a> object has not been initialized.

The <a href="https://msdn.microsoft.com/en-us/library/Ff808371(v=VS.85).aspx">ErrorString</a> property value is set to "The setup object has not been initialized. Please initialize the setup object with the InitializeInstallDefaults method."

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff808370(v=VS.85).aspx">ICertificateEnrollmentPolicyServerSetup</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff808373(v=VS.85).aspx">InitializeInstallDefaults</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff808375(v=VS.85).aspx">SetProperty</a>
 

 

