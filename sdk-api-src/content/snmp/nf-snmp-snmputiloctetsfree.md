---
UID: NF:snmp.SnmpUtilOctetsFree
title: SnmpUtilOctetsFree function (snmp.h)
description: The SnmpUtilOctetsFree function frees the memory allocated for the specified octet string. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilOctetsFree","SnmpUtilOctetsFree function [SNMP]","_snmp_snmputiloctetsfree","snmp.snmputiloctetsfree","snmp/SnmpUtilOctetsFree"]
old-location: snmp\snmputiloctetsfree.htm
tech.root: SNMP
ms.assetid: be101ab3-393c-4b1a-882d-0284715d1da4
ms.date: 12/05/2018
ms.keywords: SnmpUtilOctetsFree, SnmpUtilOctetsFree function [SNMP], _snmp_snmputiloctetsfree, snmp.snmputiloctetsfree, snmp/SnmpUtilOctetsFree
f1_keywords:
- snmp/SnmpUtilOctetsFree
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
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Snmpapi.dll
api_name:
- SnmpUtilOctetsFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpUtilOctetsFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOctetsFree</b> function frees the memory allocated for the specified octet string. This function is an element of the SNMP Utility API.


## -parameters




### -param pOctets [in]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a> structure whose memory should be freed.


## -returns



This function does not return a value.




## -remarks



Call the 
<b>SnmpUtilOctetsFree</b> function to free the memory that the 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/nf-snmp-snmputiloctetscpy">SnmpUtilOctetsCpy</a> function allocates.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/snmp/nf-snmp-snmputiloctetscpy">SnmpUtilOctetsCpy</a>
 

 

