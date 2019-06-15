---
UID: NS:windns._DnsRecordW
title: DNS_RECORDW (windns.h)
author: windows-sdk-content
description: Stores a DNS resource record (RR).
old-location: dns\dns_record.htm
tech.root: DNS
ms.assetid: ab7b96a5-346f-4e01-bb2a-885f44764590
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDNS_RECORD, *PDNS_RECORDW, DNS_RECORD, DNS_RECORD structure [DNS], DNS_RECORDW, PDNS_RECORD, PDNS_RECORD structure pointer [DNS], _DnsRecordA, _DnsRecordW, _dns_dns_record, dns.dns_record, windns/DNS_RECORD, windns/PDNS_RECORD"
ms.topic: struct
f1_keywords: ["windns/DNS_RECORD"]
req.header: windns.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_RECORD
product: Windows
targetos: Windows
req.typenames: DNS_RECORDW, *PDNS_RECORDW
req.redist: 
ms.custom: 19H1
---

# DNS_RECORDW structure


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

A value that represents the RR <a href="https://docs.microsoft.com/windows/desktop/DNS/dns-constants">DNS Record Type</a>. <b>wType</b> determines the format of <b>Data</b>. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the data type of <b>Data</b> is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_2">DNS_A_DATA</a>.


### -field wDataLength

The length, in bytes, of <b>Data</b>. For fixed-length data types, this value is the size of the corresponding data type, such as <b>sizeof(DNS_A_DATA)</b>. For the non-fixed data types, use one of the following macros to determine the length of the data: 



					

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
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

 A value that contains a bitmap of <a href="https://docs.microsoft.com/windows/desktop/DNS/dns-constants">DNS Record Flags</a>.


### -field Flags.S

A set of flags in the form of a 
<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-_dnsrecordflags">DNS_RECORD_FLAGS</a> structure.


### -field dwTtl

The DNS RR's Time To Live value (TTL), in seconds.


### -field dwReserved

Reserved. Do not use.


### -field Data

The DNS RR data type is determined by <b>wType</b> and is one of the following members:



#### SOA, Soa

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_5">DNS_SOA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SOA</b>.



#### PTR, Ptr, NS, Ns, CNAME, Cname, DNAME, Dname, MB, Mb, MD, Md, MF, Mf, MG, Mg, MR, Mr

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_3">DNS_PTR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_PTR</b>.



#### MINFO, Minfo, RP, Rp

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_7">DNS_MINFO_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MINFO</b>.



#### MX, Mx, AFSDB, Afsdb, RT, Rt

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_10">DNS_MX_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MX</b>.



#### HINFO, Hinfo, ISDN, Isdn, TXT, Txt, X25

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_11">DNS_TXT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TEXT</b>.



#### WKS, Wks

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_14">DNS_WKS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WKS</b>.



#### KEY, Key

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_18">DNS_KEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_KEY</b>.



#### SIG, Sig

The RR data type is <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms682094(v=vs.85)">DNS_SIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SIG</b>.



#### ATMA, Atma

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_34">DNS_ATMA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_ATMA</b>.



#### NXT, Nxt

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_28">DNS_NXT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NXT</b>.



#### SRV, Srv

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_30">DNS_SRV_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SRV</b>.



#### NAPTR, Naptr

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_32">DNS_NAPTR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NAPTR</b>.



#### OPT, Opt

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_26">DNS_OPT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_OPT</b>.



#### DS, Ds

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_25">DNS_DS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DS</b>.



#### RRSIG, Rrsig

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_16">DNS_RRSIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_RRSIG</b>.



#### NSEC, Nsec

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_20">DNS_NSEC_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NSEC</b>.



#### DNSKEY, Dnskey

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DNSKEY</b>.



#### TKEY, Tkey

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_35">DNS_TKEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TKEY</b>.



#### TSIG, Tsig

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_37">DNS_TSIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TSIG</b>.



#### WINS, Wins

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_40">DNS_WINS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINS</b>.



#### WINSR, WinsR, NBSTAT, Nbstat

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_41">DNS_WINSR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINSR</b>.


### -field Data.A

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_2">DNS_A_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_A</b>.


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

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_13">DNS_NULL_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NULL</b>.


### -field Data.WKS

 


### -field Data.Wks

 


### -field Data.AAAA

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_15">DNS_AAAA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_AAAA</b>.


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

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_19">DNS_DHCID_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DHCID</b>.


### -field Data.NSEC3

 


### -field Data.Nsec3

 


### -field Data.NSEC3PARAM

 


### -field Data.Nsec3Param

 


### -field Data.TLSA

 


### -field Data.Tlsa

 


### -field Data.UNKNOWN

 


### -field Data.Unknown

 


### -field Data.pDataPtr

 




##### - Data.ATMA, Atma

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_34">DNS_ATMA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_ATMA</b>.


##### - Data.DNSKEY, Dnskey

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DNSKEY</b>.


##### - Data.DS, Ds

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_25">DNS_DS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DS</b>.


##### - Data.HINFO, Hinfo, ISDN, Isdn, TXT, Txt, X25

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_11">DNS_TXT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TEXT</b>.


##### - Data.KEY, Key

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_18">DNS_KEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_KEY</b>.


##### - Data.MINFO, Minfo, RP, Rp

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_7">DNS_MINFO_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MINFO</b>.


##### - Data.MX, Mx, AFSDB, Afsdb, RT, Rt

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_10">DNS_MX_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MX</b>.


##### - Data.NAPTR, Naptr

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_32">DNS_NAPTR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NAPTR</b>.


##### - Data.NSEC, Nsec

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_20">DNS_NSEC_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NSEC</b>.


##### - Data.NXT, Nxt

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_28">DNS_NXT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NXT</b>.


##### - Data.OPT, Opt

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_26">DNS_OPT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_OPT</b>.


##### - Data.PTR, Ptr, NS, Ns, CNAME, Cname, DNAME, Dname, MB, Mb, MD, Md, MF, Mf, MG, Mg, MR, Mr

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_3">DNS_PTR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_PTR</b>.


##### - Data.RRSIG, Rrsig

Windows 7 or later: The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_16">DNS_RRSIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_RRSIG</b>.


##### - Data.SIG, Sig

The RR data type is <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms682094(v=vs.85)">DNS_SIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SIG</b>.


##### - Data.SOA, Soa

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_5">DNS_SOA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SOA</b>.


##### - Data.SRV, Srv

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_30">DNS_SRV_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SRV</b>.


##### - Data.TKEY, Tkey

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_35">DNS_TKEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TKEY</b>.


##### - Data.TSIG, Tsig

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_37">DNS_TSIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TSIG</b>.


##### - Data.WINS, Wins

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_40">DNS_WINS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINS</b>.


##### - Data.WINSR, WinsR, NBSTAT, Nbstat

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_41">DNS_WINSR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINSR</b>.


##### - Data.WKS, Wks

The RR data type is <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_14">DNS_WKS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WKS</b>.


## -remarks



When building a 
<b>DNS_RECORD</b> list as an input argument for the various DNS update routines found in the DNS API, all flags in the 
<b>DNS_RECORD</b> structure should be set to zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_15">DNS_AAAA_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_34">DNS_ATMA_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_2">DNS_A_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_19">DNS_DHCID_DATA</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_25">DNS_DS_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_18">DNS_KEY_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_27">DNS_LOC_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_7">DNS_MINFO_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_10">DNS_MX_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_32">DNS_NAPTR_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_20">DNS_NSEC_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_13">DNS_NULL_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_28">DNS_NXT_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_26">DNS_OPT_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_3">DNS_PTR_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_16">DNS_RRSIG_DATA</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms682094(v=vs.85)">DNS_SIG_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_5">DNS_SOA_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_30">DNS_SRV_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_35">DNS_TKEY_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_37">DNS_TSIG_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_11">DNS_TXT_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_41">DNS_WINSR_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_40">DNS_WINS_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-__unnamed_struct_14">DNS_WKS_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsextractrecordsfrommessage_utf8">DnsExtractRecordsFromMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsmodifyrecordsinset_a">DnsModifyRecordsInSet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsrecordcompare">DnsRecordCompare</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsrecordcopyex">DnsRecordCopyEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsrecordsetcompare">DnsRecordSetCompare</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsrecordsetdetach">DnsRecordSetDetach</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsreplacerecordseta">DnsReplaceRecordSet</a>
 

 

