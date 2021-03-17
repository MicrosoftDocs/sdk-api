---
UID: NS:wincrypt._CRL_DIST_POINT_NAME
title: CRL_DIST_POINT_NAME (wincrypt.h)
description: Identifies a location from which the CRL can be obtained.
helpviewer_keywords: ["*PCRL_DIST_POINT_NAME","CRL_DIST_POINT_FULL_NAME","CRL_DIST_POINT_ISSUER_RDN_NAME","CRL_DIST_POINT_NAME","CRL_DIST_POINT_NAME structure [Security]","CRL_DIST_POINT_NO_NAME","PCRL_DIST_POINT_NAME","PCRL_DIST_POINT_NAME structure pointer [Security]","_crypto2_crl_dist_point_name","security.crl_dist_point_name","wincrypt/CRL_DIST_POINT_NAME","wincrypt/PCRL_DIST_POINT_NAME"]
old-location: security\crl_dist_point_name.htm
tech.root: security
ms.assetid: f47283c3-34f5-4611-b041-456d28d85dbe
ms.date: 12/05/2018
ms.keywords: '*PCRL_DIST_POINT_NAME, CRL_DIST_POINT_FULL_NAME, CRL_DIST_POINT_ISSUER_RDN_NAME, CRL_DIST_POINT_NAME, CRL_DIST_POINT_NAME structure [Security], CRL_DIST_POINT_NO_NAME, PCRL_DIST_POINT_NAME, PCRL_DIST_POINT_NAME structure pointer [Security], _crypto2_crl_dist_point_name, security.crl_dist_point_name, wincrypt/CRL_DIST_POINT_NAME, wincrypt/PCRL_DIST_POINT_NAME'
req.header: wincrypt.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRL_DIST_POINT_NAME, *PCRL_DIST_POINT_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_DIST_POINT_NAME
 - wincrypt/_CRL_DIST_POINT_NAME
 - PCRL_DIST_POINT_NAME
 - wincrypt/PCRL_DIST_POINT_NAME
 - CRL_DIST_POINT_NAME
 - wincrypt/CRL_DIST_POINT_NAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRL_DIST_POINT_NAME
---

# CRL_DIST_POINT_NAME structure


## -description

The <b>CRL_DIST_POINT_NAME</b> structure identifies a location from which the CRL can be obtained. When <b>CRL_DIST_POINT_NAME</b> is used, different forms of the CRL distribution point name appear in the <b>FullName</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure. An application need not be able to process all of the name forms in the structure. It can use a distribution point if at least one name form can be processed.

If no name forms for a distribution point can be processed, an application can still use the certificate, provided requisite revocation information can be obtained from another source such as a distribution point of the <a href="/windows/desktop/SecGloss/c-gly">certification authority's</a> (CA's) directory entry.

## -struct-fields

### -field dwDistPointNameChoice

Indicates the variant used for the name data contained in the union. The following values are defined: 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_DIST_POINT_NO_NAME"></a><a id="crl_dist_point_no_name"></a><dl>
<dt><b>CRL_DIST_POINT_NO_NAME</b></dt>
</dl>
</td>
<td width="60%">
No distribution point name is provided.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_DIST_POINT_FULL_NAME"></a><a id="crl_dist_point_full_name"></a><dl>
<dt><b>CRL_DIST_POINT_FULL_NAME</b></dt>
</dl>
</td>
<td width="60%">
The distribution point name is in the <b>FullName</b> member of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_DIST_POINT_ISSUER_RDN_NAME"></a><a id="crl_dist_point_issuer_rdn_name"></a><dl>
<dt><b>CRL_DIST_POINT_ISSUER_RDN_NAME</b></dt>
</dl>
</td>
<td width="60%">
Currently not implemented.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.FullName

A
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure containing an array of alternative names specifying the CRL distribution point in one of several different forms. One of the most common uses a URL in the form "http://…" to specify the location of the CRL.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_point">CRL_DIST_POINT</a>