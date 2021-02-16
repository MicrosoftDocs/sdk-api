---
UID: NF:certif.ICertServerPolicy.SetCertificateExtension
title: ICertServerPolicy::SetCertificateExtension (certif.h)
description: Adds a new extension to the certificate.
helpviewer_keywords: ["CCertServerPolicy object [Security]","SetCertificateExtension method","EXTENSION_CRITICAL_FLAG","EXTENSION_DISABLE_FLAG","ICertServerPolicy interface [Security]","SetCertificateExtension method","ICertServerPolicy.SetCertificateExtension","ICertServerPolicy::SetCertificateExtension","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","SetCertificateExtension","SetCertificateExtension method [Security]","SetCertificateExtension method [Security]","CCertServerPolicy object","SetCertificateExtension method [Security]","ICertServerPolicy interface","_certsrv_icertserverpolicy_setcertificateextension","certif/ICertServerPolicy::SetCertificateExtension","security.icertserverpolicy_setcertificateextension"]
old-location: security\icertserverpolicy_setcertificateextension.htm
tech.root: security
ms.assetid: aed8b621-3881-41fe-b7a3-657fecdab351
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],SetCertificateExtension method, EXTENSION_CRITICAL_FLAG, EXTENSION_DISABLE_FLAG, ICertServerPolicy interface [Security],SetCertificateExtension method, ICertServerPolicy.SetCertificateExtension, ICertServerPolicy::SetCertificateExtension, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, SetCertificateExtension, SetCertificateExtension method [Security], SetCertificateExtension method [Security],CCertServerPolicy object, SetCertificateExtension method [Security],ICertServerPolicy interface, _certsrv_icertserverpolicy_setcertificateextension, certif/ICertServerPolicy::SetCertificateExtension, security.icertserverpolicy_setcertificateextension
req.header: certif.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - ICertServerPolicy::SetCertificateExtension
 - certif/ICertServerPolicy::SetCertificateExtension
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
 - ICertServerPolicy.SetCertificateExtension
 - CCertServerPolicy.SetCertificateExtension
---

# ICertServerPolicy::SetCertificateExtension


## -description

The <b>SetCertificateExtension</b> method adds a new extension to the certificate.

## -parameters

### -param strExtensionName [in]

Specifies the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the extension to set. The string must be 31 or less nonnull characters in length.

### -param Type [in]

Specifies the type of extension being set. The <i>Type</i> parameter must agree with the data type of <b>pvarValue</b> that is set in the <b>vt</b> field of the <b>VARIANT</b> structure. The <i>Type</i> parameter can be set to one of the following types. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
</dl>
</td>
<td width="60%">
Signed long data.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Date/time.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
The extension value is set as is and is assumed to be ASN.1 encoded if necessary.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The extension value will be ASN.1 encoded as an IA5 string before it is placed in the new certificate.

<div class="alert"><b>Note</b>  You should use <b>PROPTYPE_STRING</b> for an extension value that consists of a single URL only if you want the URL to be automatically encoded as an IA5 string. Otherwise, encode the URL as an IA5 string yourself and pass the encoded value as <b>PROPTYPE_BINARY</b>.</div>
<div> </div>
</td>
</tr>
</table>

### -param ExtFlags [in]

Specifies the flags for the extension being set. Use a value of zero if no flag is to be set, or use one of the following flag values. You can join these flags together by using the <b>OR</b> operator, and you can also join them by using the <b>OR</b> operator with policy private extension flags (the high 8 bits of the EXTENSION_POLICY_MASK field). 




						

<div class="alert"><b>Note</b>  When <i>ExtFlags</i> is set to EXTENSION_DISABLE_FLAG, the extension will be disabled in the server log and will not be added to the certificate.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EXTENSION_CRITICAL_FLAG"></a><a id="extension_critical_flag"></a><dl>
<dt><b>EXTENSION_CRITICAL_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This is a critical extension.

</td>
</tr>
<tr>
<td width="40%"><a id="EXTENSION_DISABLE_FLAG"></a><a id="extension_disable_flag"></a><dl>
<dt><b>EXTENSION_DISABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Extension will not be used.

</td>
</tr>
</table>

### -param pvarValue [in]

Specifies the value associated with the extension. Note the value's <b>VARIANT</b> type must agree with the <i>Type</i> parameter, as shown in the following table. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
</dl>
</td>
<td width="60%">
VT_I4

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
VT_DATE

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
VT_BSTR

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
VT_BSTR

</td>
</tr>
</table>

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Use extensions to include additional information with the certificate, such as supplemental subject or usage information. For more information, see <a href="/windows/desktop/SecCrypto/extension-handlers">Extension Handlers</a>.

Call the <b>SetCertificateExtension</b> method from your implementation of the <a href="/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy2::VerifyRequest</a> method. You must call 
the <a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a> method before calling the <b>SetCertificateExtension</b> method.

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a>