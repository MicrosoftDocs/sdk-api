---
UID: NF:certenroll.IX509Enrollment.InstallResponse
title: IX509Enrollment::InstallResponse
author: windows-sdk-content
description: Installs a certificate chain on the end-entity computer.
old-location: security\ix509enrollment_installresponse_method.htm
tech.root: seccertenroll
ms.assetid: 4ad33092-71c4-4ae1-a3a6-cef376d04c2d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AllowNoOutstandingRequest, AllowNone, AllowUntrustedCertificate, AllowUntrustedRoot, IX509Enrollment interface [Security],InstallResponse method, IX509Enrollment.InstallResponse, IX509Enrollment::InstallResponse, InstallResponse, InstallResponse method [Security], InstallResponse method [Security],IX509Enrollment interface, certenroll/IX509Enrollment::InstallResponse, security.ix509enrollment_installresponse_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IX509Enrollment.InstallResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Enrollment::InstallResponse


## -description


The <b>InstallResponse</b> method installs a certificate chain on the end-entity computer. The byte array that contains the response is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard.  You must specify  the DER-encoded byte array in a string that is either a pure binary sequence or is Unicode encoded. This method is web enabled.


## -parameters




### -param Restrictions [in]

An <a href="https://msdn.microsoft.com/070cadd8-08cf-44ce-a8b7-39a4fb11e724">InstallResponseRestrictionFlags</a> enumeration value that specifies the type of certificates that can be installed. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AllowNone"></a><a id="allownone"></a><a id="ALLOWNONE"></a><dl>
<dt><b><b>AllowNone</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Do not install untrusted certificates or certificates for which there is no corresponding request.

</td>
</tr>
<tr>
<td width="40%"><a id="AllowNoOutstandingRequest"></a><a id="allownooutstandingrequest"></a><a id="ALLOWNOOUTSTANDINGREQUEST"></a><dl>
<dt><b><b>AllowNoOutstandingRequest</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Create the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> from the certificate response rather than from the dummy certificate. This makes the dummy certificate optional. If this value is not set, the dummy certificate must exist, and the private key is extracted from it.

</td>
</tr>
<tr>
<td width="40%"><a id="AllowUntrustedCertificate"></a><a id="allowuntrustedcertificate"></a><a id="ALLOWUNTRUSTEDCERTIFICATE"></a><dl>
<dt><b><b>AllowUntrustedCertificate</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Install untrusted end entity and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> certificates. Certification authority certificates include root and subordinate CA certificates. End entity certificates are installed to the personal store, and CA certificates are installed to the certification authority store.

</td>
</tr>
<tr>
<td width="40%"><a id="AllowUntrustedRoot"></a><a id="allowuntrustedroot"></a><a id="ALLOWUNTRUSTEDROOT"></a><dl>
<dt><b><b>AllowUntrustedRoot</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Perform the same action as the <b>AllowUntrustedCertificate</b> flag but also installs the certificate even if the certificate chain cannot be built because the root is not trusted. <div class="alert"><b>Note</b>  On Windows Vista, the behavior of this flag is the same as that defined for the <b>AllowUntrustedCertificate</b> flag. Beginning with Windows Vista with SP1, you can install a certificate that chains up to an untrusted root.</div>
<div> </div>


</td>
</tr>
</table>
 


### -param strResponse [in]

A <b>BSTR</b> variable that contains the DER-encoded response.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of encoding applied to  the string that contains the DER-encoded response.


### -param strPassword [in, optional]

An optional password for the certificate installation. This can be  <b>NULL</b> or an empty string to indicate that  no password is used.  If there is a password, clear it from memory when you have finished using it by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.

Beginning with Windows 8 and Windows Server 2012, a <b>NULL</b> or empty password may mean that the PFX packet was created in the <a href="https://msdn.microsoft.com/e8bd54b1-946f-4c65-8a86-96f0dbec07ff">PFXExportCertStoreEx</a> function by using the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag. If so, the PFX was encrypted to an Active Directory group. For more information, see  <b>PFXExportCertStoreEx</b> and <a href="https://msdn.microsoft.com/2c83774a-f2df-4d28-9abd-e39aa507ba88">PFXImportCertStore</a>.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This method was called from the web and either <b>AllowNoOutstandingRequest</b> or <b>AllowUntrustedCertificate</b> was specified in the <i>Restrictions</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ARITHMETIC_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The length of the string that contains the password exceeds 64 kilobytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The enrollment object has not been initialized.

</td>
</tr>
</table>
 




## -remarks




The <b>InstallResponse</b> method:

<ol>
<li>Retrieves the dummy certificate from the external store.</li>
<li>Retrieves the certificate contained in the response and installs it on the computer.</li>
<li>Copies properties from the dummy certificate in the external store onto the newly installed certificate in the personal store.</li>
</ol>


Before calling the <b>InstallResponse</b> method, you must initialize the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/3bf4ce4a-6556-403c-8334-a6bf01f074a3">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/04cb00af-f786-4548-bee3-2cc5083278c3">InitializeFromRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/44a934f4-9ae9-4f52-9d44-f5fcf30f3837">InitializeFromTemplateName</a>
</li>
</ul>


If you call this method from the web, you can specify only <b>AllowNone</b> or <b>AllowUntrustedRoot</b> in the <i>Restrictions</i> parameter. If you specify <b>AllowNoOutstandingRequest</b> or <b>AllowUntrustedCertificate</b>, the method returns an <b>E_ACCESSDENIED</b> error.




## -see-also




<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

