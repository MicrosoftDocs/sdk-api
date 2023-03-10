---
UID: NN:certenroll.ICspStatuses
title: ICspStatuses (certenroll.h)
description: Contains information about a cryptographic provider/algorithm pair. (ICspStatuses)
helpviewer_keywords: ["ICspStatuses","ICspStatuses interface [Security]","ICspStatuses interface [Security]","described","certenroll/ICspStatuses","security.icspstatuses"]
old-location: security\icspstatuses.htm
tech.root: security
ms.assetid: 73d0f3a7-7afd-42c9-88db-911531c50137
ms.date: 12/05/2018
ms.keywords: ICspStatuses, ICspStatuses interface [Security], ICspStatuses interface [Security],described, certenroll/ICspStatuses, security.icspstatuses
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
 - ICspStatuses
 - certenroll/ICspStatuses
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
 - ICspStatuses
---

# ICspStatuses interface


## -description

The <b>ICspStatuses</b> interface defines methods and properties that can be used to manage a collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects. The <b>ICspStatus</b> interface contains information about a  cryptographic provider/algorithm pair.   The collection object is created when you call the following properties and methods.<table>
<tr>
<th>Property/Method</th>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformations-getcspstatusesfromoperations">GetCspStatusesFromOperations</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
</td>
<td>Creates an <b>ICspStatuses</b> collection for a specified algorithm type and optional provider information.<div class="alert"><b>Note</b>  The Certificate Enrollment Control uses an <b>ICspStatuses</b> collection only for private key asymmetric (encryption, signing, and key exchange) algorithm  selection.</div>
<div> </div>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-getcspstatuses">GetCspStatuses</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <b>ICspStatuses</b> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cspstatuses">CspStatuses</a>
</td>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <b>ICspStatuses</b> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as identified by the IX509PrivateKey object associated with the certificate request.</td>
</tr>
</table>

## -inheritance

The <b>ICspStatuses</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspStatuses</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
