---
UID: NF:certenroll.IX509EnrollmentHelper.AddEnrollmentServer
title: IX509EnrollmentHelper::AddEnrollmentServer
author: windows-sdk-content
description: Saves certificate enrollment server (CES) access credentials in the credential cache.
old-location: security\ix509enrollmenthelper_addenrollmentserver.htm
tech.root: SecCertEnroll
ms.assetid: a354fc02-299d-472c-9821-1509e299ccb9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddEnrollmentServer, AddEnrollmentServer method [Security], AddEnrollmentServer method [Security],IX509EnrollmentHelper interface, IX509EnrollmentHelper interface [Security],AddEnrollmentServer method, IX509EnrollmentHelper.AddEnrollmentServer, IX509EnrollmentHelper::AddEnrollmentServer, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/IX509EnrollmentHelper::AddEnrollmentServer, security.ix509enrollmenthelper_addenrollmentserver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentHelper.AddEnrollmentServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509EnrollmentHelper.AddEnrollmentServer
: 
---

# IX509EnrollmentHelper::AddEnrollmentServer


## -description


The <b>AddEnrollmentServer</b> method saves certificate enrollment server (CES) access credentials in the credential cache. This method is web enabled.


## -parameters




### -param strEnrollmentServerURI [in]

A <b>BSTR</b> that contains the certificate enrollment server URL.


### -param authFlags [in]

An <a href="https://msdn.microsoft.com/84a7e6e3-dfbb-4c27-af63-e521103e1b00">X509EnrollmentAuthFlags</a> enumeration value that specifies the client authentication type. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509AuthAnonymous"></a><a id="x509authanonymous"></a><a id="X509AUTHANONYMOUS"></a><dl>
<dt><b>X509AuthAnonymous</b></dt>
</dl>
</td>
<td width="60%">
Anonymous authentication. Set the <i>strCredential</i> and <i>strPassword</i> parameters to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthKerberos"></a><a id="x509authkerberos"></a><a id="X509AUTHKERBEROS"></a><dl>
<dt><b>X509AuthKerberos</b></dt>
</dl>
</td>
<td width="60%">
Kerberos authentication. Set the <i>strCredential</i> and <i>strPassword</i> parameters to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthUsername"></a><a id="x509authusername"></a><a id="X509AUTHUSERNAME"></a><dl>
<dt><b>X509AuthUsername</b></dt>
</dl>
</td>
<td width="60%">
Clear text user name and password authentication. Set the <i>strCredential</i> and <i>strPassword</i> parameters to the user name and associated password. These strings are encrypted before transmission and are stored securely in the credential vault on the certificate enrollment server.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthCertificate"></a><a id="x509authcertificate"></a><a id="X509AUTHCERTIFICATE"></a><dl>
<dt><b>X509AuthCertificate</b></dt>
</dl>
</td>
<td width="60%">
Client authentication certificate installed on the local computer and used by the server to verify the identity of the client. Set the <i>strPassword</i> parameter to <b>NULL</b> and set the certificate thumbprint, a 20-byte SHA1 hash of the certificate, in the <i>strCredential</i> parameter.

</td>
</tr>
</table>
 


### -param strCredential [in]

A <b>BSTR</b> that contains the credential.


### -param strPassword [in]

A <b>BSTR</b> that contains a clear text password.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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
The <i>strEnrollmentServerURI</i> parameter cannot be <b>NULL</b> or empty.

If X509AuthAnonymous or X509AuthKerberos is specified in the <i>authFlags</i> parameter, the <i>strCredential</i> parameter must not be <b>NULL</b>.

If X509AuthCertificate is specified in the <i>authFlags</i> parameter, the <i>strCredential</i> parameter must be <b>NULL</b>.

If X509AuthCertificateis specified in the <i>authFlags</i> parameter, the <i>strPassword</i> parameter must be <b>NULL</b>, but <i>strCredential</i> parameter must not be.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ARITHMETIC_OVERFLOW)</b></dt>
</dl>
</td>
<td width="60%">
The <i>strPassword</i>, <i>strCredential</i>, or <i>strEnrollmentServerURI</i> parameters exceed 64,000 characters or contain embedded null characters.

</td>
</tr>
</table>
 




## -remarks



The <i>strCredential</i> and <i>strPassword</i> arguments change depending on the value specified in the <i>authFlags</i> argument as shown in the following table.

<table>
<tr>
<th><i>flag</i> parameter </th>
<th><i>strCredential</i> parameter</th>
<th><i>strPassword</i> parameter</th>
</tr>
<tr>
<td>X509AuthAnonymous</td>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
</tr>
<tr>
<td>X509AuthKerberos</td>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
</tr>
<tr>
<td>X509AuthUsername</td>
<td>Clear text user name recognized by the CEP server.</td>
<td>Clear text password associated with the user name.</td>
</tr>
<tr>
<td>X509AuthCertificate</td>
<td>Contains a 20 byte SHA-1 hash (thumbprint) of the certificate.</td>
<td><b>NULL</b></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a>
 

 

