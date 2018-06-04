---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICertificateEnrollmentServerSetup::GetProperty


## -description


The <b>GetProperty</b> method retrieves a <a href="https://msdn.microsoft.com/9FA6B249-B5B3-40AF-B175-CD5933D468B9">CESSetupProperty</a> enumeration value for the Certificate Enrollment Web Service (CES) configuration.


## -parameters




### -param propertyId [in]

A <a href="https://msdn.microsoft.com/9FA6B249-B5B3-40AF-B175-CD5933D468B9">CESSetupProperty</a> enumeration value that specifies the property value to retrieve. For more information, see Remarks.


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
The <i>propertyId</i> argument is not a member of the <a href="https://msdn.microsoft.com/9FA6B249-B5B3-40AF-B175-CD5933D468B9">CESSetupProperty</a> enumeration type.

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
The <a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a> object has not been initialized.

The <a href="https://msdn.microsoft.com/D4322BE8-1CED-47D0-98C2-D5D7C151DEAB">ErrorString</a> property value is set to "The setup object has not been initialized. Please initialize the setup object with the InitializeInstallDefaults method."

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/9FA6B249-B5B3-40AF-B175-CD5933D468B9">CESSetupProperty</a> enumeration type contains the following values:<ul>
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




<a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a>
 

 

