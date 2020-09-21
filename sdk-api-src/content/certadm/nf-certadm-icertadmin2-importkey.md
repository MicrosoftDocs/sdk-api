---
UID: NF:certadm.ICertAdmin2.ImportKey
title: ICertAdmin2::ImportKey (certadm.h)
description: Adds an encrypted key set to an item in the Certificate Services database. The key set is encrypted to one or several key recovery agent (KRA) certificates.
helpviewer_keywords: ["CR_IN_BASE64","CR_IN_BASE64HEADER","CR_IN_BINARY","ICertAdmin2 interface [Security]","ImportKey method","ICertAdmin2.ImportKey","ICertAdmin2::ImportKey","IKF_OVERWRITE","ImportKey","ImportKey method [Security]","ImportKey method [Security]","ICertAdmin2 interface","certadm/ICertAdmin2::ImportKey","security.icertadmin2_importkey"]
old-location: security\icertadmin2_importkey.htm
tech.root: security
ms.assetid: d71f20d7-5b27-41e5-adc1-6f0ae4160210
ms.date: 12/05/2018
ms.keywords: CR_IN_BASE64, CR_IN_BASE64HEADER, CR_IN_BINARY, ICertAdmin2 interface [Security],ImportKey method, ICertAdmin2.ImportKey, ICertAdmin2::ImportKey, IKF_OVERWRITE, ImportKey, ImportKey method [Security], ImportKey method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::ImportKey, security.icertadmin2_importkey
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
 - ICertAdmin2::ImportKey
 - certadm/ICertAdmin2::ImportKey
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
 - ICertAdmin2.ImportKey
---

# ICertAdmin2::ImportKey


## -description

The <b>ImportKey</b> method adds an encrypted key set to an item in the Certificate Services database. The  key set is encrypted to one or several key recovery agent (KRA) certificates.

## -parameters

### -param strConfig [in]

String value that represents a valid configuration string for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA)  in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>ImportKey</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

<b>LONG</b> value that represents the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> ID in the Certificates Services database. If the serial number (passed in as <i>strCertHash</i>) is to be used instead of the request ID, use zero for this value.

### -param strCertHash [in]

String value that represents the certificate hash. For <i>strCertHash</i> to be used, you must specify a value of zero for <i>RequestId</i>.

### -param Flags [in]

Specifies the format of the key. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64HEADER"></a><a id="cr_in_base64header"></a><dl>
<dt><b>CR_IN_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format with begin or end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64"></a><a id="cr_in_base64"></a><dl>
<dt><b>CR_IN_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format without begin or end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BINARY"></a><a id="cr_in_binary"></a><dl>
<dt><b>CR_IN_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary format.

</td>
</tr>
</table>
 

Additionally, the following value can be combined with the format value by using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKF_OVERWRITE"></a><a id="ikf_overwrite"></a><dl>
<dt><b>IKF_OVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
Any existing KRA encoded information is overwritten.

</td>
</tr>
</table>

### -param strKey [in]

String value that represents the KRA key information.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>