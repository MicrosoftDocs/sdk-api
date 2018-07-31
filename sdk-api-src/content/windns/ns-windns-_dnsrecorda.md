---
UID: NS:windns._DnsRecordA
title: "_DnsRecordA"
author: windows-sdk-content
description: Stores a DNS resource record (RR).
old-location: dns\dns_record.htm
old-project: DNS
ms.assetid: ab7b96a5-346f-4e01-bb2a-885f44764590
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DNS_RECORD, DNS_RECORD structure [DNS], PDNS_RECORD, PDNS_RECORD structure pointer [DNS], _DnsRecordA, _DnsRecordW, _dns_dns_record, dns.dns_record, windns/DNS_RECORD, windns/PDNS_RECORD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: 
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DnsRecordA structure


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

A value that represents the RR <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Type</a>. <b>wType</b> determines the format of <b>Data</b>. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the data type of <b>Data</b> is <a href="https://msdn.microsoft.com/0fd21930-1319-4ae7-b46f-2b744f4faae9">DNS_A_DATA</a>.


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

 A value that contains a bitmap of <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Flags</a>.


### -field Flags.S

A set of flags in the form of a 
<a href="https://msdn.microsoft.com/53c1c8bc-20b0-4b15-b2b6-9c9854f73ee3">DNS_RECORD_FLAGS</a> structure.


### -field dwTtl

The DNS RR's Time To Live value (TTL), in seconds.


### -field dwReserved

Reserved. Do not use.


### -field Data

The DNS RR data type is determined by <b>wType</b> and is one of the following members:



#### SOA, Soa

The RR data type is <a href="https://msdn.microsoft.com/715cbb70-91fe-47ac-a713-1fe0701d4f8c">DNS_SOA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SOA</b>.



#### PTR, Ptr, NS, Ns, CNAME, Cname, DNAME, Dname, MB, Mb, MD, Md, MF, Mf, MG, Mg, MR, Mr

The RR data type is <a href="https://msdn.microsoft.com/8b7f8898-ac91-46da-876c-889c427068a3">DNS_PTR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_PTR</b>.



#### MINFO, Minfo, RP, Rp

The RR data type is <a href="https://msdn.microsoft.com/cd392b48-734f-462b-b893-855f07c30575">DNS_MINFO_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MINFO</b>.



#### MX, Mx, AFSDB, Afsdb, RT, Rt

The RR data type is <a href="https://msdn.microsoft.com/72a0b42e-a7af-42d2-b672-cf06d0b5d1ba">DNS_MX_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_MX</b>.



#### HINFO, Hinfo, ISDN, Isdn, TXT, Txt, X25

The RR data type is <a href="https://msdn.microsoft.com/3ff643e2-d736-45d5-8cf8-ab5e63caf44b">DNS_TXT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TEXT</b>.



#### WKS, Wks

The RR data type is <a href="https://msdn.microsoft.com/94477345-74e7-40bf-a75b-e4bf67f1c17b">DNS_WKS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WKS</b>.



#### KEY, Key

The RR data type is <a href="https://msdn.microsoft.com/d7d60322-4d06-4c57-b181-c6a38e09e1ef">DNS_KEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_KEY</b>.



#### SIG, Sig

The RR data type is <a href="https://msdn.microsoft.com/184f7a8d-5a81-4dea-ba9c-05f40042bbb5">DNS_SIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SIG</b>.



#### ATMA, Atma

The RR data type is <a href="https://msdn.microsoft.com/09df3990-36bd-4656-b5cd-792e521adf9d">DNS_ATMA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_ATMA</b>.



#### NXT, Nxt

The RR data type is <a href="https://msdn.microsoft.com/0e5370c2-30d3-4bb7-85a0-f4412f5572fd">DNS_NXT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NXT</b>.



#### SRV, Srv

The RR data type is <a href="https://msdn.microsoft.com/212db7ac-a5e3-4e58-b1c2-0eb551403dfc">DNS_SRV_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_SRV</b>.



#### NAPTR, Naptr

The RR data type is <a href="https://msdn.microsoft.com/8f576efb-4ef3-4fc0-8cf5-d373460a3b3c">DNS_NAPTR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NAPTR</b>.



#### OPT, Opt

Windows 7 or later: The RR data type is <a href="https://msdn.microsoft.com/a8e23127-a625-4206-abe8-0787b4ac0f30">DNS_OPT_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_OPT</b>.



#### DS, Ds

Windows 7 or later: The RR data type is <a href="https://msdn.microsoft.com/8624cc27-feb5-4e4a-8970-40aa1d43960e">DNS_DS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DS</b>.



#### RRSIG, Rrsig

Windows 7 or later: The RR data type is <a href="https://msdn.microsoft.com/09c2f515-acc1-402f-8e62-a0d273031633">DNS_RRSIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_RRSIG</b>.



#### NSEC, Nsec

Windows 7 or later: The RR data type is <a href="https://msdn.microsoft.com/ea446732-bc6a-4597-b164-11bfd77c07f2">DNS_NSEC_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NSEC</b>.



#### DNSKEY, Dnskey

Windows 7 or later: The RR data type is <a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DNSKEY</b>.



#### TKEY, Tkey

The RR data type is <a href="https://msdn.microsoft.com/4dad3449-3e41-47d9-89c2-10fa6e51573b">DNS_TKEY_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TKEY</b>.



#### TSIG, Tsig

The RR data type is <a href="https://msdn.microsoft.com/32077169-d319-45c0-982f-8d470cd70111">DNS_TSIG_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_TSIG</b>.



#### WINS, Wins

The RR data type is <a href="https://msdn.microsoft.com/df41c397-e662-42b4-9193-6776f9071898">DNS_WINS_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINS</b>.



#### WINSR, WinsR, NBSTAT, Nbstat

The RR data type is <a href="https://msdn.microsoft.com/a7e79e30-905f-42a5-a4de-02d71adfe95e">DNS_WINSR_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_WINSR</b>.


### -field Data.A

The RR data type is <a href="https://msdn.microsoft.com/0fd21930-1319-4ae7-b46f-2b744f4faae9">DNS_A_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_A</b>.


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

The RR data type is <a href="https://msdn.microsoft.com/c31e468f-8efd-4173-bc2c-442ee4df737f">DNS_NULL_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_NULL</b>.


### -field Data.WKS

 


### -field Data.Wks

 


### -field Data.AAAA

The RR data type is <a href="https://msdn.microsoft.com/0bc48e86-368c-431c-b67a-b7689dca8d3c">DNS_AAAA_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_AAAA</b>.


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

Windows 7 or later: The RR data type is <a href="https://msdn.microsoft.com/868846bc-9f63-4bb3-ac8d-cea34232bb41">DNS_DHCID_DATA</a>. The value of <b>wType</b> is <b>DNS_TYPE_DHCID</b>.


### -field Data.NSEC3

 


### -field Data.Nsec3

 


### -field Data.NSEC3PARAM

 


### -field Data.Nsec3Param

 


### -field Data.TLSA

 


### -field Data.Tlsa

 


### -field Data.UNKNOWN

 


### -field Data.Unknown

 


### -field Data.pDataPtr

 




## -remarks



When building a 
<b>DNS_RECORD</b> list as an input argument for the various DNS update routines found in the DNS API, all flags in the 
<b>DNS_RECORD</b> structure should be set to zero.




## -see-also




<a href="https://msdn.microsoft.com/0bc48e86-368c-431c-b67a-b7689dca8d3c">DNS_AAAA_DATA</a>



<a href="https://msdn.microsoft.com/09df3990-36bd-4656-b5cd-792e521adf9d">DNS_ATMA_DATA</a>



<a href="https://msdn.microsoft.com/0fd21930-1319-4ae7-b46f-2b744f4faae9">DNS_A_DATA</a>



<a href="https://msdn.microsoft.com/868846bc-9f63-4bb3-ac8d-cea34232bb41">DNS_DHCID_DATA</a>



<a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a>



<a href="https://msdn.microsoft.com/8624cc27-feb5-4e4a-8970-40aa1d43960e">DNS_DS_DATA</a>



<a href="https://msdn.microsoft.com/d7d60322-4d06-4c57-b181-c6a38e09e1ef">DNS_KEY_DATA</a>



<a href="https://msdn.microsoft.com/c1e05479-17f0-4993-8dcf-02036989d6dc">DNS_LOC_DATA</a>



<a href="https://msdn.microsoft.com/cd392b48-734f-462b-b893-855f07c30575">DNS_MINFO_DATA</a>



<a href="https://msdn.microsoft.com/72a0b42e-a7af-42d2-b672-cf06d0b5d1ba">DNS_MX_DATA</a>



<a href="https://msdn.microsoft.com/8f576efb-4ef3-4fc0-8cf5-d373460a3b3c">DNS_NAPTR_DATA</a>



<a href="https://msdn.microsoft.com/ea446732-bc6a-4597-b164-11bfd77c07f2">DNS_NSEC_DATA</a>



<a href="https://msdn.microsoft.com/c31e468f-8efd-4173-bc2c-442ee4df737f">DNS_NULL_DATA</a>



<a href="https://msdn.microsoft.com/0e5370c2-30d3-4bb7-85a0-f4412f5572fd">DNS_NXT_DATA</a>



<a href="https://msdn.microsoft.com/a8e23127-a625-4206-abe8-0787b4ac0f30">DNS_OPT_DATA</a>



<a href="https://msdn.microsoft.com/8b7f8898-ac91-46da-876c-889c427068a3">DNS_PTR_DATA</a>



<a href="https://msdn.microsoft.com/09c2f515-acc1-402f-8e62-a0d273031633">DNS_RRSIG_DATA</a>



<a href="https://msdn.microsoft.com/184f7a8d-5a81-4dea-ba9c-05f40042bbb5">DNS_SIG_DATA</a>



<a href="https://msdn.microsoft.com/715cbb70-91fe-47ac-a713-1fe0701d4f8c">DNS_SOA_DATA</a>



<a href="https://msdn.microsoft.com/212db7ac-a5e3-4e58-b1c2-0eb551403dfc">DNS_SRV_DATA</a>



<a href="https://msdn.microsoft.com/4dad3449-3e41-47d9-89c2-10fa6e51573b">DNS_TKEY_DATA</a>



<a href="https://msdn.microsoft.com/32077169-d319-45c0-982f-8d470cd70111">DNS_TSIG_DATA</a>



<a href="https://msdn.microsoft.com/3ff643e2-d736-45d5-8cf8-ab5e63caf44b">DNS_TXT_DATA</a>



<a href="https://msdn.microsoft.com/a7e79e30-905f-42a5-a4de-02d71adfe95e">DNS_WINSR_DATA</a>



<a href="https://msdn.microsoft.com/df41c397-e662-42b4-9193-6776f9071898">DNS_WINS_DATA</a>



<a href="https://msdn.microsoft.com/94477345-74e7-40bf-a75b-e4bf67f1c17b">DNS_WKS_DATA</a>



<a href="https://msdn.microsoft.com/0179bf3e-9243-4dd7-a2ab-e2f6f4bf4b82">DnsExtractRecordsFromMessage</a>



<a href="https://msdn.microsoft.com/4287b4e1-a7a2-4b73-b5bb-21bc639bae73">DnsModifyRecordsInSet</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/c4449a23-d6d3-4f27-a963-a84144983e5e">DnsRecordCompare</a>



<a href="https://msdn.microsoft.com/b5a74799-75fc-4489-9efa-c15b2def2ae7">DnsRecordCopyEx</a>



<a href="https://msdn.microsoft.com/008cf2ba-ccb2-430a-85d9-68d424b6938f">DnsRecordSetCompare</a>



<a href="https://msdn.microsoft.com/434dc11f-19a9-434f-a024-9cdbb560f24c">DnsRecordSetDetach</a>



<a href="https://msdn.microsoft.com/7b99f440-72fa-4cf4-9267-98f436e99a50">DnsReplaceRecordSet</a>
 

 

