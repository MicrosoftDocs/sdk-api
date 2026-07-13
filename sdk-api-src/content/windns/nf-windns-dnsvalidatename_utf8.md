---
UID: NF:windns.DnsValidateName_UTF8
title: DnsValidateName_UTF8 function (windns.h)
description: The DnsValidateName_UTF8 function (windns.h) function validates the status of a specified DNS name.
helpviewer_keywords: ["DnsValidateName","DnsValidateName function [DNS]","DnsValidateName_A","DnsValidateName_UTF8","DnsValidateName_W","_dns_dnsvalidatename","dns.dnsvalidatename","windns/DnsValidateName","windns/DnsValidateName_A","windns/DnsValidateName_UTF8","windns/DnsValidateName_W"]
old-location: dns\dnsvalidatename.htm
tech.root: DNS
ms.assetid: efdbd217-6936-42c1-a1eb-8655a62513ee
ms.date: 08/15/2022
ms.keywords: DnsValidateName, DnsValidateName function [DNS], DnsValidateName_A, DnsValidateName_UTF8, DnsValidateName_W, _dns_dnsvalidatename, dns.dnsvalidatename, windns/DnsValidateName, windns/DnsValidateName_A, windns/DnsValidateName_UTF8, windns/DnsValidateName_W
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DnsValidateName_W (Unicode) and DnsValidateName_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsValidateName_UTF8
 - windns/DnsValidateName_UTF8
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsValidateName
 - DnsValidateName_A
 - DnsValidateName_W
 - DnsValidateName_UTF8
---

# DnsValidateName_UTF8 function


## -description

The 
<b>DnsValidateName</b> function validates the status of a specified DNS name. Like many DNS functions, the 
<b>DnsValidateName</b> function type is implemented in multiple forms to facilitate different character encoding. Based on the character encoding involved, use one of the following functions:
<ul>
<li>
<b>DnsValidateName_A</b> (_A for ANSI encoding)

</li>
<li>
<b>DnsValidateName_W</b> (_W for Unicode encoding)

</li>
<li>
<b>DnsValidateName_UTF8</b> (_UTF8 for UTF-8 encoding)

</li>
</ul>

## -parameters

### -param pszName [in]

A pointer to a string that represents the DNS name to be examined.

### -param Format [in]

A <a href="/windows/desktop/api/windns/ne-windns-dns_name_format">DNS_NAME_FORMAT</a> value that specifies the format of the name to be examined.

## -returns

The 
<b>DnsValidateName</b> function has the following possible return values:

## -remarks

To verify the status of the Computer Host (single label), use the 
<b>DnsValidateName</b> function type with <b>DnsNameHostnameLabel</b> in <i>Format</i>.

The 
<b>DnsValidateName</b> function works in a progression when determining whether an error exists with a given DNS name, and returns upon finding its first error. Therefore, a DNS name that has multiple, different errors may be reported as having the first error, and could be corrected and resubmitted, only then to find the second error.

The 
<b>DnsValidateName</b> function searches for errors as follows:

<ol>
<li>Returns <b>ERROR_INVALID_NAME</b> if the DNS name:
						<ul>
<li>Is longer than 255 octets.</li>
<li>Contains a label longer than 63 octets.</li>
<li>Contains two or more consecutive dots.</li>
<li>Begins with a dot (.).</li>
<li>Contains a dot (.) if the name is submitted with <i>Format</i> set to DnsNameDomainLabel or DnsNameHostnameLabel.</li>
</ul>
</li>
<li>Next, 
<b>DnsValidateName</b> returns <b>DNS_ERROR_NUMERIC_NAME</b> if the full DNS name consists of only  numeric characters (0-9) or the first label of the DNS name consists of only numeric characters (0-9), unless <i>Format</i> is set to DnsNameDomainLabel or DnsNameDomain.</li>
<li>Then, 
<b>DnsValidateName</b> returns DNS_ERROR_NON_RFC_NAME if the DNS name:
						<ul>
<li>Contains at least one extended or Unicode character.<b>Note</b>  Windows 8 or later: <b>DnsValidateName_W</b> does not return an error if International Domain Name (IDN) encoding is enabled.

</li>
<li>Contains underscore (_), unless the underscore is a first character in a label, in the name, submitted with <i>Format</i> set to DnsNameSrvRecord.</li>
</ul>
</li>
<li>Next, 
<b>DnsValidateName</b> returns <b>DNS_ERROR_INVALID_NAME_CHAR</b> if the DNS name:
						<ul>
<li>Contains a space.</li>
<li>Contains any of the following invalid characters: { | } ~ [ \ ] ^ ' : ; &lt; = &gt; ? &amp; @ ! " # $ % ^ ` ( ) + / ,</li>
<li>Contains an asterisk (*), unless the asterisk is the first label in the multi-labeled name, submitted with <i>Format</i> set to <b>DnsNameWildcard</b>.</li>
</ul>
</li>
</ol>
<div class="alert"><b>Note</b>  If 
<b>DnsValidateName</b> returns <b>DNS_ERROR_NON_RFC_NAME</b>, the error should be handled as a warning that not all DNS servers will accept the name. When this error is received, note that the DNS Server does accept the submitted name, if appropriately configured (default configuration accepts the name as submitted when <b>DNS_ERROR_NON_RFC_NAME</b> is returned), but other DNS server software may not. Windows DNS servers do handle <b>NON_RFC_NAMES</b>.<p class="note">If 
<b>DnsValidateName</b> returns any of the following errors, <i>pszName</i> should be handled as an invalid host name:

<dl>
<dd>DNS_ERROR_NUMERIC_NAME</dd>
<dd>DNS_ERROR_INVALID_NAME_CHAR</dd>
<dd>ERROR_INVALID_NAME</dd>
</dl>
</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/windns/ne-windns-dns_name_format">DNS_NAME_FORMAT</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsnamecompare">DnsNameCompare</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>
