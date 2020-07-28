---
UID: NF:certenroll.IX509CertificateRequestPkcs10.InitializeFromTemplateName
title: IX509CertificateRequestPkcs10::InitializeFromTemplateName (certenroll.h)
description: .
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","InitializeFromTemplateName method","IX509CertificateRequestPkcs10.InitializeFromTemplateName","IX509CertificateRequestPkcs10::InitializeFromTemplateName","InitializeFromTemplateName","InitializeFromTemplateName method [Security]","InitializeFromTemplateName method [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::InitializeFromTemplateName","security.ix509certificaterequestpkcs10_initializefromtemplatename_method"]
old-location: security\ix509certificaterequestpkcs10_initializefromtemplatename_method.htm
tech.root: security
ms.assetid: 4ea746c3-b967-41b4-94ae-7b16b93ca4e4
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],InitializeFromTemplateName method, IX509CertificateRequestPkcs10.InitializeFromTemplateName, IX509CertificateRequestPkcs10::InitializeFromTemplateName, InitializeFromTemplateName, InitializeFromTemplateName method [Security], InitializeFromTemplateName method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::InitializeFromTemplateName, security.ix509certificaterequestpkcs10_initializefromtemplatename_method
f1_keywords:
- certenroll/IX509CertificateRequestPkcs10.InitializeFromTemplateName
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
- IX509CertificateRequestPkcs10.InitializeFromTemplateName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequestPkcs10::InitializeFromTemplateName


## -description


The <b>InitializeFromTemplateName</b> method initializes the certificate request by using a template.


## -parameters




### -param Context [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or administrator acting on behalf of the computer.


### -param strTemplateName [in]

A  <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a>.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeFromTemplateName</b> method creates the following collections:<ul>
<li>An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.</li>
<li>An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection populated with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers.</li>
<li>An empty <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection for attribute and extension OIDs to be suppressed from the new request.</li>
</ul>


The method then examines the template and performs the following actions:<ul>
<li>Adds the extensions specified by the template to the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>Removes the default critical extensions (XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2) from the collection if the template indicates that they are not critical. The OIDs marked critical by the template are added.</li>
<li>Sets the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Creates an asymmetric encryption algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Sets the following <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> properties from the template settings:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyusage">KeyUsage</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_length">Length</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_exportpolicy">ExportPolicy</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyprotection">KeyProtection</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_securitydescriptor">SecurityDescriptor</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_silent">Silent</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_machinecontext">MachineContext</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_algorithm">Algorithm</a>
</li>
</ul>
</li>
</ul>


If the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CSPInformations</a> property is <b>NULL</b>, the method creates an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a> collection from the providers installed on the computer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
 

 

