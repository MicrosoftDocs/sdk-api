---
UID: NS:winsnmp.smiCNTR64
title: smiCNTR64 (winsnmp.h)
description: The WinSNMP smiCNTR64 structure contains a 64-bit unsigned integer value. The structure represents a 64-bit counter.
helpviewer_keywords: ["*smiLPCNTR64","_snmp_smicntr64_str","smiCNTR64","smiCNTR64 structure [SNMP]","smiLPCNTR64","smiLPCNTR64 structure pointer [SNMP]","snmp.smicntr64_str","winsnmp/smiCNTR64","winsnmp/smiLPCNTR64"]
old-location: snmp\smicntr64_str.htm
tech.root: SNMP
ms.assetid: 224b162c-a9b3-4b71-a9ed-b15a51934498
ms.date: 12/05/2018
ms.keywords: '*smiLPCNTR64, _snmp_smicntr64_str, smiCNTR64, smiCNTR64 structure [SNMP], smiLPCNTR64, smiLPCNTR64 structure pointer [SNMP], snmp.smicntr64_str, winsnmp/smiCNTR64, winsnmp/smiLPCNTR64'
req.header: winsnmp.h
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
req.typenames: smiCNTR64, *smiLPCNTR64
req.redist: 
ms.custom: 19H1
f1_keywords:
 - smiLPCNTR64
 - winsnmp/smiLPCNTR64
 - smiCNTR64
 - winsnmp/smiCNTR64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsnmp.h
api_name:
 - smiCNTR64
---

# smiCNTR64 structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>smiCNTR64</b> structure contains a 64-bit unsigned integer value. The structure represents a 64-bit counter.

## -struct-fields

### -field hipart

Specifies the high-order 32 bits of the counter.

### -field lopart

Specifies the low-order 32 bits of the counter.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvb">SnmpGetVb</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/SNMP/winsnmp-structures">WinSNMP Structures</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a>

