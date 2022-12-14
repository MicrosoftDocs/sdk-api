---
UID: NN:certenroll.ICspStatus
title: ICspStatus (certenroll.h)
description: Contains information about a cryptographic provider/algorithm pair. (ICspStatus)
helpviewer_keywords: ["ICspStatus","ICspStatus interface [Security]","ICspStatus interface [Security]","described","certenroll/ICspStatus","security.icspstatus"]
old-location: security\icspstatus.htm
tech.root: security
ms.assetid: 30cc43c8-6ef3-49ad-8cff-9a5b7389ff68
ms.date: 12/05/2018
ms.keywords: ICspStatus, ICspStatus interface [Security], ICspStatus interface [Security],described, certenroll/ICspStatus, security.icspstatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspStatus
 - certenroll/ICspStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatus
---

# ICspStatus interface


## -description

An <b>ICspStatus</b> object contains information about a  cryptographic provider/algorithm pair. The object is primarily used by the Certificate Enrollment Control to enable a user to select which cryptographic providers and algorithms to use when creating a certificate request. It can be retrieved, either alone or in an  <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection, by calling the following properties or methods:<table>
<tr>
<th>Property/Method</th>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-getcspstatusfromoperations">GetCspStatusFromOperations</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>
</td>
<td>Creates an <b>ICspStatus</b> object for the first supported algorithm that is consistent with a specified algorithm object identifier (OID) and algorithm type.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformations-getcspstatusesfromoperations">GetCspStatusesFromOperations</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
</td>
<td>Creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection for a specified algorithm type and optional provider information.<div class="alert"><b>Note</b>  The Certificate Enrollment Control uses an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection only for private key asymmetric (encryption, signing, and key exchange) algorithm  selection.</div>
<div> </div>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformations-getcspstatusfromprovidername">GetCspStatusFromProviderName</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
</td>
<td>Creates an <b>ICspStatus</b> object for a legacy provider by provider name and supported key operations.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspstatus">CspStatus</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
</td>
<td>Specifies or retrieves an <b>ICspStatus</b> object. The  object is typically created during the enrollment process.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-getcspstatuses">GetCspStatuses</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cspstatuses">CspStatuses</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as identified by the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object associated with the certificate request.</td>
</tr>
</table>
 



Because cryptographic providers typically support more than one algorithm, multiple <b>ICspStatus</b> objects may be created and returned when you call any of the preceding properties or methods that return a collection. This is shown by the following  illustration:

<img alt="Structure of the ICspStatuses collection showing individual ICspStatus objects" src="./images/ICSPStatuses.png"/>

You can use the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_enrollmentstatus">EnrollmentStatus</a> property on an <b>ICspStatus</b> object to retrieve an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a> object that defines the following properties:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a> property specifies whether the provider/algorithm pair can be displayed in a user interface.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property specifies or retrieves a value that indicates whether the status of a specific item is monitored during the enrollment process.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_status">Status</a> property identifies the status of the enrollment process.</li>
</ul>

## -inheritance

The <b>ICspStatus</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspStatus</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
