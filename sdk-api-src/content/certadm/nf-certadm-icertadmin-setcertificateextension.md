---
UID: NF:certadm.ICertAdmin.SetCertificateExtension
title: ICertAdmin::SetCertificateExtension (certadm.h)
description: Adds a new extension to the certificate issued in response to a certificate request. This method was first defined by the ICertAdmin interface.
helpviewer_keywords: ["CCertAdmin interface [Security]","SetCertificateExtension method","EXTENSION_CRITICAL_FLAG","EXTENSION_DISABLE_FLAG","ICertAdmin interface [Security]","SetCertificateExtension method","ICertAdmin.SetCertificateExtension","ICertAdmin2 interface [Security]","SetCertificateExtension method","ICertAdmin2::SetCertificateExtension","ICertAdmin::SetCertificateExtension","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","SetCertificateExtension","SetCertificateExtension method [Security]","SetCertificateExtension method [Security]","CCertAdmin interface","SetCertificateExtension method [Security]","ICertAdmin interface","SetCertificateExtension method [Security]","ICertAdmin2 interface","certadm/ICertAdmin2::SetCertificateExtension","certadm/ICertAdmin::SetCertificateExtension","security.icertadmin2_setcertificateextension"]
old-location: security\icertadmin2_setcertificateextension.htm
tech.root: security
ms.assetid: d26061da-acc3-45d8-93de-f2d431d350a6
ms.date: 12/05/2018
ms.keywords: CCertAdmin interface [Security],SetCertificateExtension method, EXTENSION_CRITICAL_FLAG, EXTENSION_DISABLE_FLAG, ICertAdmin interface [Security],SetCertificateExtension method, ICertAdmin.SetCertificateExtension, ICertAdmin2 interface [Security],SetCertificateExtension method, ICertAdmin2::SetCertificateExtension, ICertAdmin::SetCertificateExtension, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, SetCertificateExtension, SetCertificateExtension method [Security], SetCertificateExtension method [Security],CCertAdmin interface, SetCertificateExtension method [Security],ICertAdmin interface, SetCertificateExtension method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::SetCertificateExtension, certadm/ICertAdmin::SetCertificateExtension, security.icertadmin2_setcertificateextension
req.header: certadm.h
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
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin::SetCertificateExtension
 - certadm/ICertAdmin::SetCertificateExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.SetCertificateExtension
 - ICertAdmin.SetCertificateExtension
 - CCertAdmin.SetCertificateExtension
---

# ICertAdmin::SetCertificateExtension


## -description

The <b>SetCertificateExtension</b> method adds a new extension to the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> issued in response to a <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This method was first defined by the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

For this method to succeed, the certificate request must be pending.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>SetCertificateExtension</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

Specifies the ID of the certificate request.

### -param strExtensionName [in]

Specifies the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the extension to set. The string must be 31 or fewer non-NULL characters in length.

### -param Type [in]

Specifies the type of extension being set. The <i>Type</i> parameter must agree with the data type of the <i>pvarValue</i> parameter. This data type is set in the <b>vt</b> field of the <b>VARIANT</b> structure.

This parameter can be one of the following values.

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
Signed long data

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Date/time

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

### -param Flags [in]

Specifies the flags for the extension being set. If no flag is to be set, use a value of zero. You can combine these flags with a bitwise-<b>OR</b> operation and also with policy private extension flags (the high 8 bits of the EXTENSION_POLICY_MASK field). 




						

<div class="alert"><b>Note</b>  When the <i>Flags</i> parameter is set to EXTENSION_DISABLE_FLAG, the extension will be disabled in the server log and will not be added to the certificate.</div>
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
The extension will not be used.

</td>
</tr>
</table>

### -param pvarValue [in]

Specifies the value associated with the extension.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>