---
UID: NF:certenc.ICertEncodeAltName.SetNameEntry
title: ICertEncodeAltName::SetNameEntry (certenc.h)
description: Sets a name at a specified index of the alternate name array.
helpviewer_keywords: ["CCertEncodeAltName object [Security]","SetNameEntry method","CERT_ALT_NAME_DIRECTORY_NAME","CERT_ALT_NAME_DNS_NAME","CERT_ALT_NAME_IP_ADDRESS","CERT_ALT_NAME_OTHER_NAME","CERT_ALT_NAME_REGISTERED_ID","CERT_ALT_NAME_RFC822_NAME","CERT_ALT_NAME_URL","ICertEncodeAltName interface [Security]","SetNameEntry method","ICertEncodeAltName.SetNameEntry","ICertEncodeAltName::SetNameEntry","SetNameEntry","SetNameEntry method [Security]","SetNameEntry method [Security]","CCertEncodeAltName object","SetNameEntry method [Security]","ICertEncodeAltName interface","_certsrv_icertencodealtname_setnameentry","certenc/ICertEncodeAltName::SetNameEntry","security.icertencodealtname_setnameentry"]
old-location: security\icertencodealtname_setnameentry.htm
tech.root: security
ms.assetid: 5da07c09-9213-4604-b058-5e69df646b09
ms.date: 12/05/2018
ms.keywords: CCertEncodeAltName object [Security],SetNameEntry method, CERT_ALT_NAME_DIRECTORY_NAME, CERT_ALT_NAME_DNS_NAME, CERT_ALT_NAME_IP_ADDRESS, CERT_ALT_NAME_OTHER_NAME, CERT_ALT_NAME_REGISTERED_ID, CERT_ALT_NAME_RFC822_NAME, CERT_ALT_NAME_URL, ICertEncodeAltName interface [Security],SetNameEntry method, ICertEncodeAltName.SetNameEntry, ICertEncodeAltName::SetNameEntry, SetNameEntry, SetNameEntry method [Security], SetNameEntry method [Security],CCertEncodeAltName object, SetNameEntry method [Security],ICertEncodeAltName interface, _certsrv_icertencodealtname_setnameentry, certenc/ICertEncodeAltName::SetNameEntry, security.icertencodealtname_setnameentry
req.header: certenc.h
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
req.dll: Certenc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertEncodeAltName::SetNameEntry
 - certenc/ICertEncodeAltName::SetNameEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeAltName.SetNameEntry
 - CCertEncodeAltName.SetNameEntry
---

# ICertEncodeAltName::SetNameEntry


## -description

The <b>SetNameEntry</b> method sets a name at a specified index of the  alternate name array.

Before using this method, you must call 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-reset">ICertEncodeAltName::Reset</a> so that the object knows how many elements are in the array.

## -parameters

### -param NameIndex [in]

Zero-based index that specifies the index of the alternate name entry to set.

If the <i>NameChoice</i> parameter is CERT_ALT_NAME_OTHER_NAME, OR (|) the index value with EAN_NAMEOBJECTID (defined as 0x80000000) to set the OID. Otherwise, the binary value is set.

### -param NameChoice [in]

Specifies the name choice. The name choice indicates the type of the alternate name so that it can be used correctly. It must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_DIRECTORY_NAME"></a><a id="cert_alt_name_directory_name"></a><dl>
<dt><b>CERT_ALT_NAME_DIRECTORY_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is a directory name.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_DNS_NAME"></a><a id="cert_alt_name_dns_name"></a><dl>
<dt><b>CERT_ALT_NAME_DNS_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is an IA5 string specifying a DNS (Domain Name System) name in the format host.entity.domain.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_IP_ADDRESS"></a><a id="cert_alt_name_ip_address"></a><dl>
<dt><b>CERT_ALT_NAME_IP_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The name is an octet string that represents an Internet Protocol address.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_REGISTERED_ID"></a><a id="cert_alt_name_registered_id"></a><dl>
<dt><b>CERT_ALT_NAME_REGISTERED_ID</b></dt>
</dl>
</td>
<td width="60%">
The name is a registered <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_RFC822_NAME"></a><a id="cert_alt_name_rfc822_name"></a><dl>
<dt><b>CERT_ALT_NAME_RFC822_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is an email address.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_URL"></a><a id="cert_alt_name_url"></a><dl>
<dt><b>CERT_ALT_NAME_URL</b></dt>
</dl>
</td>
<td width="60%">
The name is an IA5 string that contains a URL in the format <i>Service</i><b>://</b><i>HostName</i><b>/</b><i>Path</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_OTHER_NAME"></a><a id="cert_alt_name_other_name"></a><dl>
<dt><b>CERT_ALT_NAME_OTHER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name consists of an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a binary <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

</td>
</tr>
</table>

### -param strName [in]

Specifies the alternate name.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodealtname">ICertEncodeAltName</a>