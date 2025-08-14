---
UID: NS:windnsdef._DnsRecordA
title: DNS_RECORDA (windnsdef.h)
description: Stores a DNS resource record (RR). (ANSI)
helpviewer_keywords: ["*PDNS_RECORD","*PDNS_RECORDA","DNS_RECORD","DNS_RECORD structure [DNS]","DNS_RECORDA","PDNS_RECORD","PDNS_RECORD structure pointer [DNS]","_DnsRecordA","_DnsRecordW","_dns_dns_record","dns.dns_record","windnsdef/DNS_RECORD","windnsdef/PDNS_RECORD"]
old-location: dns\dns_record.htm
tech.root: DNS
ms.assetid: ab7b96a5-346f-4e01-bb2a-885f44764590
ms.date: 01/15/2025
ms.keywords: '*PDNS_RECORD, *PDNS_RECORDA, DNS_RECORD, DNS_RECORD structure [DNS], DNS_RECORDA, PDNS_RECORD, PDNS_RECORD structure pointer [DNS], _DnsRecordA, _DnsRecordW, _dns_dns_record, dns.dns_record, windnsdef/DNS_RECORD, windnsdef/PDNS_RECORD'
req.header: windnsdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DNS_RECORDA, *PDNS_RECORDA
req.redist: 
f1_keywords:
 - _DnsRecordA
 - windnsdef/_DnsRecordA
 - PDNS_RECORDA
 - windnsdef/PDNS_RECORDA
 - DNS_RECORDA
 - windnsdef/DNS_RECORDA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windnsdef.h
api_name:
 - DNS_RECORD
---

# DNS_RECORDA structure


## -description

The 
<b>DNS_RECORD</b> structure stores a DNS resource record (RR).

## -struct-fields

### -field pNext

A pointer to the next 
<b>DNS_RECORD</b> structure.

### -field pName

A pointer to a string that represents the domain name of the record set. This must be in the string format that corresponds to the function called, such as ANSI, Unicode, or UTF8.

### -field wType

A value that represents the RR <a href="/windows/win32/DNS/dns-constants">DNS Record Type</a>. <b>wType</b> determines the format of <b>Data</b>. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the data type of <b>Data</b> is <a href="/windows/win32/api/windnsdef/nf-windns-dnsquery_a">DNS_A_DATA</a>.

### -field wDataLength

The length, in bytes, of <b>Data</b>. For fixed-length data types, this value is the size of the corresponding data type, such as <b>sizeof(DNS_A_DATA)</b>. For the non-fixed data types, use one of the following macros to determine the length of the data: 

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#define DNS_NULL_RECORD_LENGTH(ByteCount) (sizeof(DWORD) + (ByteCount))
#define DNS_WKS_RECORD_LENGTH(ByteCount) (sizeof(DNS_WKS_DATA) + (ByteCount-1))
#define DNS_WINS_RECORD_LENGTH(IpCount) (sizeof(DNS_WINS_DATA) + ((IpCount-1) * sizeof(IP_ADDRESS)))
#define DNS_TEXT_RECORD_LENGTH(StringCount) (sizeof(DWORD) + ((StringCount) * sizeof(PCHAR)))
</pre>
</td>
</tr>
</table></span></div>

### -field Flags

### -field Flags.DW

 A value that contains a bitmap of <a href="/windows/win32/DNS/dns-constants">DNS Record Flags</a>.

### -field Flags.S

A set of flags in the form of a 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_record_flags">DNS_RECORD_FLAGS</a> structure.

### -field dwTtl

The DNS RR's Time To Live value (TTL), in seconds.

### -field dwReserved

Reserved. Do not use.

### -field Data

The DNS RR data type is determined by <b>wType</b> and is one of the following members:

#### SOA, Soa

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_soa_dataw">DNS_SOA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SOA</b>.

#### PTR, Ptr, NS, Ns, CNAME, Cname, DNAME, Dname, MB, Mb, MD, Md, MF, Mf, MG, Mg, MR, Mr

The RR data type is <a href="/windows/win32/api/windnsdef/nf-windns-dnsquery_w">DNS_PTR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_PTR</b>.

#### MINFO, Minfo, RP, Rp

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_minfo_dataw">DNS_MINFO_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MINFO</b>.

#### MX, Mx, AFSDB, Afsdb, RT, Rt

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_mx_dataa">DNS_MX_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MX</b>.

#### HINFO, Hinfo, ISDN, Isdn, TXT, Txt, X25

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_txt_dataw">DNS_TXT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TEXT</b>.

#### WKS, Wks

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_wks_data">DNS_WKS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WKS</b>.

#### KEY, Key

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_key_data">DNS_KEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_KEY</b>.

#### SIG, Sig

The RR data type is <a href="/previous-versions/windows/desktop/legacy/ms682094(v=vs.85)">DNS_SIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SIG</b>.

#### ATMA, Atma

The RR data type is [DNS_ATMA_DATA](./ns-windnsdef-dns_atma_data.md). The value of <b>wType</b> is <b>DNS_TYPE_ATMA</b>.

#### NXT, Nxt

The RR data type is [DNS_NXT_DATA](./ns-windnsdef-dns_nxt_dataa.md). The value of <b>wType</b> is <b>DNS_TYPE_NXT</b>.

#### SRV, Srv

The RR data type is [DNS_SRV_DATA](./ns-windnsdef-dns_srv_dataa.md). The value of <b>wType</b> is <b>DNS_TYPE_SRV</b>.

#### NAPTR, Naptr

The RR data type is [DNS_NAPTR_DATA](./ns-windnsdef-dns_naptr_dataa.md). The value of <b>wType</b> is <b>DNS_TYPE_NAPTR</b>.

#### OPT, Opt

Windows 7 or later: The RR data type is [DNS_OPT_DATA](./ns-windnsdef-dns_opt_data.md). The value of <b>wType</b> is <b>DNS_TYPE_OPT</b>.

#### DS, Ds

Windows 7 or later: The RR data type is [DNS_DS_DATA](./ns-windnsdef-dns_ds_data.md). The value of <b>wType</b> is <b>DNS_TYPE_DS</b>.

#### RRSIG, Rrsig

Windows 7 or later: The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_sig_dataw">DNS_RRSIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_RRSIG</b>.

#### NSEC, Nsec

Windows 7 or later: The RR data type is [DNS_NSEC_DATA](./ns-windnsdef-dns_nsec_dataa.md). The value of <b>wType</b> is <b>DNS_TYPE_NSEC</b>.

#### DNSKEY, Dnskey

Windows 7 or later: The RR data type is <a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DNSKEY</b>.

#### TKEY, Tkey

The RR data type is [DNS_TKEY_DATA](./ns-windnsdef-dns_tkey_dataa.md). The value of <b>wType</b> is <b>DNS_TYPE_TKEY</b>.

#### TSIG, Tsig

The RR data type is [DNS_TSIG_DATA](./ns-windnsdef-dns_tsig_dataa.md). The value of <b>wType</b> is <b>DNS_TYPE_TSIG</b>.

#### WINS, Wins

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_wins_data">DNS_WINS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINS</b>.

#### WINSR, WinsR, NBSTAT, Nbstat

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_winsr_dataw">DNS_WINSR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINSR</b>.

### -field Data.A

The RR data type is <a href="/windows/win32/api/windnsdef/nf-windns-dnsquery_a">DNS_A_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_A</b>.

### -field Data.SOA

### -field Data.Soa

### -field Data.PTR

### -field Data.Ptr

### -field Data.NS

### -field Data.Ns

### -field Data.CNAME

### -field Data.Cname

### -field Data.DNAME

### -field Data.Dname

### -field Data.MB

### -field Data.Mb

### -field Data.MD

### -field Data.Md

### -field Data.MF

### -field Data.Mf

### -field Data.MG

### -field Data.Mg

### -field Data.MR

### -field Data.Mr

### -field Data.MINFO

### -field Data.Minfo

### -field Data.RP

### -field Data.Rp

### -field Data.MX

### -field Data.Mx

### -field Data.AFSDB

### -field Data.Afsdb

### -field Data.RT

### -field Data.Rt

### -field Data.HINFO

### -field Data.Hinfo

### -field Data.ISDN

### -field Data.Isdn

### -field Data.TXT

### -field Data.Txt

### -field Data.X25

### -field Data.Null

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_null_data">DNS_NULL_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NULL</b>.

### -field Data.WKS

### -field Data.Wks

### -field Data.AAAA

The RR data type is <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_aaaa_data">DNS_AAAA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_AAAA</b>.

### -field Data.KEY

### -field Data.Key

### -field Data.SIG

### -field Data.Sig

### -field Data.ATMA

### -field Data.Atma

### -field Data.NXT

### -field Data.Nxt

### -field Data.SRV

### -field Data.Srv

### -field Data.NAPTR

### -field Data.Naptr

### -field Data.OPT

### -field Data.Opt

### -field Data.DS

### -field Data.Ds

### -field Data.RRSIG

### -field Data.Rrsig

### -field Data.NSEC

### -field Data.Nsec

### -field Data.DNSKEY

### -field Data.Dnskey

### -field Data.TKEY

### -field Data.Tkey

### -field Data.TSIG

### -field Data.Tsig

### -field Data.WINS

### -field Data.Wins

### -field Data.WINSR

### -field Data.WinsR

### -field Data.NBSTAT

### -field Data.Nbstat

### -field Data.DHCID

Windows 7 or later: The RR data type is <a href="/windows/win32/api/windnsdef/ns-windns-dns_dhcid_data">DNS_DHCID_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DHCID</b>.

### -field Data.NSEC3

### -field Data.Nsec3

### -field Data.NSEC3PARAM

### -field Data.Nsec3Param

### -field Data.TLSA

### -field Data.Tlsa

### -field Data.SVCB

Type: **[DNS_SVCB_DATA](/windows/win32/api/windnsdef/ns-windnsdef-dns_svcb_data)**

TBD

### -field Data.Svcb

Type: **[DNS_SVCB_DATA](/windows/win32/api/windnsdef/ns-windnsdef-dns_svcb_data)**

TBD

### -field Data.UNKNOWN

### -field Data.Unknown

### -field Data.pDataPtr

## -remarks

When building a 
<b>DNS_RECORD</b> list as an input argument for the various DNS update routines found in the DNS API, all flags in the 
<b>DNS_RECORD</b> structure should be set to zero.

> [!NOTE]
> The windns.h header defines DNS_RECORD as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_aaaa_data">DNS_AAAA_DATA</a>



[DNS_ATMA_DATA](./ns-windnsdef-dns_atma_data.md)



<a href="/windows/win32/api/windnsdef/nf-windns-dnsquery_a">DNS_A_DATA</a>



<a href="/windows/win32/api/windnsdef/ns-windns-dns_dhcid_data">DNS_DHCID_DATA</a>



<a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a>



[DNS_DS_DATA](./ns-windnsdef-dns_ds_data.md)



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_key_data">DNS_KEY_DATA</a>



[DNS_LOC_DATA](./ns-windnsdef-dns_loc_data.md)



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_minfo_dataw">DNS_MINFO_DATA</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_mx_dataa">DNS_MX_DATA</a>



[DNS_NAPTR_DATA](./ns-windnsdef-dns_naptr_dataa.md)



[DNS_NSEC_DATA](./ns-windnsdef-dns_nsec_dataa.md)



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_null_data">DNS_NULL_DATA</a>



[DNS_NXT_DATA](./ns-windnsdef-dns_nxt_dataa.md)



[DNS_OPT_DATA](./ns-windnsdef-dns_opt_data.md)



<a href="/windows/win32/api/windnsdef/nf-windns-dnsquery_w">DNS_PTR_DATA</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_sig_dataw">DNS_RRSIG_DATA</a>



<a href="/previous-versions/windows/desktop/legacy/ms682094(v=vs.85)">DNS_SIG_DATA</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_soa_dataw">DNS_SOA_DATA</a>



[DNS_SRV_DATA](./ns-windnsdef-dns_srv_dataa.md)



[DNS_TKEY_DATA](./ns-windnsdef-dns_tkey_dataa.md)



[DNS_TSIG_DATA](./ns-windnsdef-dns_tsig_dataa.md)



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_txt_dataw">DNS_TXT_DATA</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_winsr_dataw">DNS_WINSR_DATA</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_wins_data">DNS_WINS_DATA</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_wks_data">DNS_WKS_DATA</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsextractrecordsfrommessage_utf8">DnsExtractRecordsFromMessage</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsmodifyrecordsinset_a">DnsModifyRecordsInSet</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsquery_a">DnsQuery</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsrecordcompare">DnsRecordCompare</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsrecordcopyex">DnsRecordCopyEx</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsrecordsetcompare">DnsRecordSetCompare</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsrecordsetdetach">DnsRecordSetDetach</a>



<a href="/windows/win32/api/windnsdef/nf-windns-dnsreplacerecordseta">DnsReplaceRecordSet</a>
