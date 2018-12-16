---
UID: NF:certcli.ICertRequest3.GetIssuedCertificate2
title: ICertRequest3::GetIssuedCertificate2
author: windows-sdk-content
description: Retrieves a certificate's disposition by specifying either the request ID string or the certificate serial number.
old-location: security\icertrequest3_getissuedcertificate2.htm
tech.root: seccrypto
ms.assetid: c311acaf-983b-4d61-a674-0fc6b475d212
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertRequest object [Security],GetIssuedCertificate2 method, CR_DISP_DENIED, CR_DISP_ERROR, CR_DISP_INCOMPLETE, CR_DISP_ISSUED, CR_DISP_ISSUED_OUT_OF_BAND, CR_DISP_UNDER_SUBMISSION, GetIssuedCertificate2, GetIssuedCertificate2 method [Security], GetIssuedCertificate2 method [Security],CCertRequest object, GetIssuedCertificate2 method [Security],ICertRequest3 class, ICertRequest3 class [Security],GetIssuedCertificate2 method, ICertRequest3.GetIssuedCertificate2, ICertRequest3::GetIssuedCertificate2, certcli/ICertRequest3::GetIssuedCertificate2, security.icertrequest3_getissuedcertificate2
ms.topic: method
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.GetIssuedCertificate2
 - CCertRequest.GetIssuedCertificate2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest3::GetIssuedCertificate2


## -description


The <b>GetIssuedCertificate2</b> method retrieves a certificate's disposition by specifying either the request ID string or the certificate serial number.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Services</a> server. The string can be either an HTTPS URL for an enrollment server or in the form <i>ComputerName</i><b>\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the server, and <i>CAName</i> is the common name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.


<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>An HTTPS URL is not supported as an input.


### -param strRequestId [in]

A <b>BSTR</b> value that represents the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> ID in the Certificates Services database. Set this parameter to <b>NULL</b> if the serial number (passed in as <i>strSerialNumber</i>) is to be used instead of the request ID.

Use the  <a href="https://msdn.microsoft.com/09afc06f-95e8-4519-b0c7-36da5986e077">ICertRequest3::GetRequestIdString</a> method to obtain the request ID string.


### -param strSerialNumber [in]

A <b>BSTR</b> value that represents the certificate serial number, as issued by the CA. The string must specify the serial number as an even number of hexadecimal digits. If necessary, a zero can be prefixed to the number to produce an even number of digits. However, no more than one leading zero may be used.

The <i>strSerialNumber</i> value is only used when the <i>strRequestId</i> is set to <b>NULL</b>.


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
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Long</b> that represents the certificate's disposition.




## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

