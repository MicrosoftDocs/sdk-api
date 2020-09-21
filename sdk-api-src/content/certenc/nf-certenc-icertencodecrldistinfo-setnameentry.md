---
UID: NF:certenc.ICertEncodeCRLDistInfo.SetNameEntry
title: ICertEncodeCRLDistInfo::SetNameEntry (certenc.h)
description: Sets a name at a specified index of a distribution point in a certificate revocation list (CRL) distribution information array.
helpviewer_keywords: ["CCertEncodeCRLDistInfo object [Security]","SetNameEntry method","CERT_ALT_NAME_DNS_NAME","CERT_ALT_NAME_REGISTERED_ID","CERT_ALT_NAME_RFC822_NAME","CERT_ALT_NAME_URL","ICertEncodeCRLDistInfo interface [Security]","SetNameEntry method","ICertEncodeCRLDistInfo.SetNameEntry","ICertEncodeCRLDistInfo::SetNameEntry","SetNameEntry","SetNameEntry method [Security]","SetNameEntry method [Security]","CCertEncodeCRLDistInfo object","SetNameEntry method [Security]","ICertEncodeCRLDistInfo interface","_certsrv_icertencodecrldistinfo_setnameentry","certenc/ICertEncodeCRLDistInfo::SetNameEntry","security.icertencodecrldistinfo_setnameentry"]
old-location: security\icertencodecrldistinfo_setnameentry.htm
tech.root: security
ms.assetid: fe33265a-8c75-4e16-8178-3569cf30d8e4
ms.date: 12/05/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],SetNameEntry method, CERT_ALT_NAME_DNS_NAME, CERT_ALT_NAME_REGISTERED_ID, CERT_ALT_NAME_RFC822_NAME, CERT_ALT_NAME_URL, ICertEncodeCRLDistInfo interface [Security],SetNameEntry method, ICertEncodeCRLDistInfo.SetNameEntry, ICertEncodeCRLDistInfo::SetNameEntry, SetNameEntry, SetNameEntry method [Security], SetNameEntry method [Security],CCertEncodeCRLDistInfo object, SetNameEntry method [Security],ICertEncodeCRLDistInfo interface, _certsrv_icertencodecrldistinfo_setnameentry, certenc/ICertEncodeCRLDistInfo::SetNameEntry, security.icertencodecrldistinfo_setnameentry
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
 - ICertEncodeCRLDistInfo::SetNameEntry
 - certenc/ICertEncodeCRLDistInfo::SetNameEntry
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
 - ICertEncodeCRLDistInfo.SetNameEntry
 - CCertEncodeCRLDistInfo.SetNameEntry
---

# ICertEncodeCRLDistInfo::SetNameEntry


## -description

The <b>SetNameEntry</b> method sets a name at a specified index of a distribution point in a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution information array.

## -parameters

### -param DistPointIndex [in]

Specifies the index of the CRL distribution point for which to set the name. The first value is at index zero.

### -param NameIndex [in]

Specifies the index of the name entry to set. The first value is at index zero.

### -param NameChoice [in]

Specifies the name choice of the name being set. The name choice indicates the type of the name so that it can be used correctly. The name choice must be one of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<td width="40%"><a id="CERT_ALT_NAME_DNS_NAME"></a><a id="cert_alt_name_dns_name"></a><dl>
<dt><b>CERT_ALT_NAME_DNS_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is an IA5 string specifying a DNS (Domain Name System) name in the format host.entity.domain.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ALT_NAME_URL"></a><a id="cert_alt_name_url"></a><dl>
<dt><b>CERT_ALT_NAME_URL</b></dt>
</dl>
</td>
<td width="60%">
The name is an IA5 string specifying a URL in the format <i>Service</i><b>://</b><i>HostName</i><b>/</b><i>Path</i>.

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
</table>

### -param strName [in]

Specifies the name.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodecrldistinfo">ICertEncodeCRLDistInfo</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getname">ICertEncodeCRLDistInfo::GetName</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getnamechoice">ICertEncodeCRLDistInfo::GetNameChoice</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnamecount">ICertEncodeCRLDistInfo::SetNameCount</a>