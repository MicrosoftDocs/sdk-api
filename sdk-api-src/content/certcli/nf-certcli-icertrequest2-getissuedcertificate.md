---
UID: NF:certcli.ICertRequest2.GetIssuedCertificate
title: ICertRequest2::GetIssuedCertificate (certcli.h)
description: Retrieves a certificate's disposition by specifying either the request ID or the certificate serial number.
helpviewer_keywords: ["CCertRequest object [Security]","GetIssuedCertificate method","CR_DISP_DENIED","CR_DISP_ERROR","CR_DISP_INCOMPLETE","CR_DISP_ISSUED","CR_DISP_ISSUED_OUT_OF_BAND","CR_DISP_UNDER_SUBMISSION","GetIssuedCertificate","GetIssuedCertificate method [Security]","GetIssuedCertificate method [Security]","CCertRequest object","GetIssuedCertificate method [Security]","ICertRequest interface","GetIssuedCertificate method [Security]","ICertRequest2 interface","GetIssuedCertificate method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetIssuedCertificate method","ICertRequest2 interface [Security]","GetIssuedCertificate method","ICertRequest2.GetIssuedCertificate","ICertRequest2::GetIssuedCertificate","ICertRequest3 interface [Security]","GetIssuedCertificate method","ICertRequest3::GetIssuedCertificate","ICertRequest::GetIssuedCertificate","_certsrv_icertrequest2_getissuedcertificate","certcli/ICertRequest2::GetIssuedCertificate","certcli/ICertRequest3::GetIssuedCertificate","certcli/ICertRequest::GetIssuedCertificate","security.icertrequest2_getissuedcertificate"]
old-location: security\icertrequest2_getissuedcertificate.htm
tech.root: security
ms.assetid: ea7f6013-a55d-4a76-9c9e-df180ba9bb79
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetIssuedCertificate method, CR_DISP_DENIED, CR_DISP_ERROR, CR_DISP_INCOMPLETE, CR_DISP_ISSUED, CR_DISP_ISSUED_OUT_OF_BAND, CR_DISP_UNDER_SUBMISSION, GetIssuedCertificate, GetIssuedCertificate method [Security], GetIssuedCertificate method [Security],CCertRequest object, GetIssuedCertificate method [Security],ICertRequest interface, GetIssuedCertificate method [Security],ICertRequest2 interface, GetIssuedCertificate method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetIssuedCertificate method, ICertRequest2 interface [Security],GetIssuedCertificate method, ICertRequest2.GetIssuedCertificate, ICertRequest2::GetIssuedCertificate, ICertRequest3 interface [Security],GetIssuedCertificate method, ICertRequest3::GetIssuedCertificate, ICertRequest::GetIssuedCertificate, _certsrv_icertrequest2_getissuedcertificate, certcli/ICertRequest2::GetIssuedCertificate, certcli/ICertRequest3::GetIssuedCertificate, certcli/ICertRequest::GetIssuedCertificate, security.icertrequest2_getissuedcertificate
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest2::GetIssuedCertificate
 - certcli/ICertRequest2::GetIssuedCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.GetIssuedCertificate
 - ICertRequest2.GetIssuedCertificate
 - ICertRequest.GetIssuedCertificate
 - CCertRequest.GetIssuedCertificate
---

# ICertRequest2::GetIssuedCertificate


## -description

The <b>GetIssuedCertificate</b> method retrieves a certificate's disposition by specifying either the request ID or the certificate serial number.

This method is effectively  the same as calling <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">ICertRequest3::RetrievePending</a>, with the additional capability of specifying a serial number for the certificate in question.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The string can be either an HTTPS URL for an enrollment server or in the form <i>ComputerName</i><b>\\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the server, and <i>CAName</i> is the common name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>An HTTPS URL is not supported as an input.

### -param RequestId [in]

A <b>LONG</b> value that represents the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> ID in the Certificates Services database. Use –1 for this value if the serial number (passed in as <i>strSerialNumber</i>) is to be used instead of the request ID.

### -param strSerialNumber [in]

A <b>BSTR</b> value that represents the certificate serial number, as issued by the CA. For <i>strSerialNumber</i> to be used, you must specify a value of –1 for <i>RequestId</i>.

### -param pDisposition [out, retval]

A pointer to a <b>LONG</b> value that represents the certificate's disposition. The disposition is one of the following values. 




               

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_DISP_DENIED"></a><a id="cr_disp_denied"></a><dl>
<dt><b>CR_DISP_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Request denied.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_DISP_ERROR"></a><a id="cr_disp_error"></a><dl>
<dt><b>CR_DISP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Request failed.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_DISP_INCOMPLETE"></a><a id="cr_disp_incomplete"></a><dl>
<dt><b>CR_DISP_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Request did not complete.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_DISP_ISSUED"></a><a id="cr_disp_issued"></a><dl>
<dt><b>CR_DISP_ISSUED</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_DISP_ISSUED_OUT_OF_BAND"></a><a id="cr_disp_issued_out_of_band"></a><dl>
<dt><b>CR_DISP_ISSUED_OUT_OF_BAND</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued separately.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_DISP_UNDER_SUBMISSION"></a><a id="cr_disp_under_submission"></a><dl>
<dt><b>CR_DISP_UNDER_SUBMISSION</b></dt>
</dl>
</td>
<td width="60%">
Request taken under submission.

</td>
</tr>
</table>

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Long</b> that represents the certificate's disposition.