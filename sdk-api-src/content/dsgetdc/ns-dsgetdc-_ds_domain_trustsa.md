---
UID: NS:dsgetdc._DS_DOMAIN_TRUSTSA
title: "_DS_DOMAIN_TRUSTSA"
author: windows-driver-content
description: Used with the DsEnumerateDomainTrusts function to contain trust data for a domain.
old-location: ad\ds_domain_trusts.htm
old-project: AD
ms.assetid: cd260fd1-dc38-4405-95ba-097a23faf668
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*PDS_DOMAIN_TRUSTSA, DS_DOMAIN_DIRECT_INBOUND, DS_DOMAIN_DIRECT_OUTBOUND, DS_DOMAIN_IN_FOREST, DS_DOMAIN_NATIVE_MODE, DS_DOMAIN_PRIMARY, DS_DOMAIN_TREE_ROOT, DS_DOMAIN_TRUSTS, DS_DOMAIN_TRUSTS structure [Active Directory], DS_DOMAIN_TRUSTSA, DS_DOMAIN_TRUSTSW, PDS_DOMAIN_TRUSTS, PDS_DOMAIN_TRUSTS structure pointer [Active Directory], _DS_DOMAIN_TRUSTSA, _glines_ds_domain_trusts, ad.ds__domain__trusts, ad.ds_domain_trusts, dsgetdc/DS_DOMAIN_TRUSTS, dsgetdc/DS_DOMAIN_TRUSTSA, dsgetdc/DS_DOMAIN_TRUSTSW, dsgetdc/PDS_DOMAIN_TRUSTS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_DOMAIN_TRUSTSW (Unicode) and DS_DOMAIN_TRUSTSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DS_DOMAIN_TRUSTSA, *PDS_DOMAIN_TRUSTSA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dsgetdc.h
api_name:
-	DS_DOMAIN_TRUSTS
-	DS_DOMAIN_TRUSTSA
-	DS_DOMAIN_TRUSTSW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DS_DOMAIN_TRUSTSA structure


## -description


The <b>DS_DOMAIN_TRUSTS</b> structure is used with the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function to contain  trust data for a domain.


## -struct-fields




### -field NetbiosDomainName

Pointer to a null-terminated string that contains the NetBIOS name of the domain.


### -field DnsDomainName

Pointer to a null-terminated string that contains the DNS name of the domain. This member may be <b>NULL</b>.


### -field Flags

Contains a set of flags that specify more data about the domain trust. This can be zero or a combination of one or more of the following values.



#### DS_DOMAIN_IN_FOREST (1 (0x1))

The domain represented by this structure is a member of the same forest as the server specified in the <i>ServerName</i> parameter of the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function.



#### DS_DOMAIN_DIRECT_OUTBOUND (2 (0x2))

The domain represented by this structure is directly trusted by the domain that the server specified in the <i>ServerName</i> parameter of the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function is a member of.



#### DS_DOMAIN_TREE_ROOT (4 (0x4))

The domain represented by this structure is the root of a tree and a member of the same forest as the server specified in the <i>ServerName</i> parameter of the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function.



#### DS_DOMAIN_PRIMARY (8 (0x8))

The domain represented by this structure is the primary domain of the server specified in the <i>ServerName</i> parameter of the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function.



#### DS_DOMAIN_NATIVE_MODE (16 (0x10))

The domain represented by this structure is running in the Windows 2000 native mode.



#### DS_DOMAIN_DIRECT_INBOUND (32 (0x20))

The domain represented by this structure directly trusts the domain that the server specified in the <i>ServerName</i> parameter of the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function is a member of.


### -field ParentIndex

Contains the index in the <i>Domains</i> array returned by the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function that corresponds to the parent domain of the domain represented by this structure. This member is only valid if the all of the following conditions are met:

<ul>
<li>The <b>DS_DOMAIN_IN_FOREST</b> flag was specified in the <i>Flags</i> parameter of the <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> function.</li>
<li>The <b>Flags</b> member of this structure does not contain the <b>DS_DOMAIN_TREE_ROOT</b> flag.</li>
</ul>

### -field TrustType

Contains a value that indicates the type of trust represented by this structure. Possible values for this member are documented in the <b>TrustType</b> member of the <a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structure.


### -field TrustAttributes

Contains a value that indicates the attributes of the trust represented by this structure. Possible values for this member are documented in the <b>TrustAttribute</b> member of the <a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structure.


### -field DomainSid

Contains the security identifier of the domain represented by this structure.


### -field DomainGuid

Contains the GUID of the domain represented by this structure.


## -see-also




<a href="https://msdn.microsoft.com/4df5f356-a39b-40a4-9e62-994ad27df3a9">Directory Service Structures</a>



<a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>
 

 

