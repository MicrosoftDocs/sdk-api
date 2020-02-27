---
UID: NS:snmp.__unnamed_struct_1
title: AsnObjectIdentifier (snmp.h)
description: The AsnObjectIdentifier structure represents object identifiers. This structure is used by multiple SNMP functions. This structure is not used by the WinSNMP API functions.
old-location: snmp\asnobjectidentifier_str.htm
tech.root: SNMP
ms.assetid: 695e5581-00df-49af-8abe-1dd1b25cb215
ms.date: 12/05/2018
ms.keywords: AsnObjectIdentifier, AsnObjectIdentifier structure [SNMP], AsnObjectName, _snmp_asnobjectidentifier_str, snmp.asnobjectidentifier_str, snmp/AsnObjectIdentifier
f1_keywords:
- snmp/AsnObjectIdentifier
dev_langs:
- c++
req.header: snmp.h
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
- Snmp.h
api_name:
- AsnObjectIdentifier
targetos: Windows
req.typenames: AsnObjectIdentifier
req.redist: 
ms.custom: 19H1
---

# AsnObjectIdentifier structure


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>AsnObjectIdentifier</b> structure represents object identifiers. This structure is used by multiple SNMP functions. This structure is not used by the 
<a href="https://docs.microsoft.com/windows/desktop/SNMP/winsnmp-api">WinSNMP API</a> functions.


## -struct-fields




### -field idLength

Specifies the number of integers in the object identifier.


### -field ids

Pointer to an array of integers that represents the object identifier.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SNMP/snmp-structures">SNMP Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>
 

 

