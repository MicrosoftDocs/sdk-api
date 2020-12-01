---
UID: NF:snmp.SnmpUtilOctetsCpy
title: SnmpUtilOctetsCpy function (snmp.h)
description: The SnmpUtilOctetsCpy function copies the variable pointed to by the pOctetsSrc parameter to the variable pointed to by the pOctetsDst parameter.
helpviewer_keywords: ["SnmpUtilOctetsCpy","SnmpUtilOctetsCpy function [SNMP]","_snmp_snmputiloctetscpy","snmp.snmputiloctetscpy","snmp/SnmpUtilOctetsCpy"]
old-location: snmp\snmputiloctetscpy.htm
tech.root: SNMP
ms.assetid: 5ea92551-f6af-431d-8bf8-5b6c576f3392
ms.date: 12/05/2018
ms.keywords: SnmpUtilOctetsCpy, SnmpUtilOctetsCpy function [SNMP], _snmp_snmputiloctetscpy, snmp.snmputiloctetscpy, snmp/SnmpUtilOctetsCpy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpUtilOctetsCpy
 - snmp/SnmpUtilOctetsCpy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilOctetsCpy
---

# SnmpUtilOctetsCpy function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOctetsCpy</b> function copies the variable pointed to by the <i>pOctetsSrc</i> parameter to the variable pointed to by the <i>pOctetsDst</i> parameter. The function allocates any necessary memory for the destination's copy. The 
<b>SnmpUtilOctetsCpy</b> function is an element of the SNMP Utility API.

## -parameters

### -param pOctetsDst [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a> structure to receive the copy.

### -param pOctetsSrc [in]

Pointer to an 
<b>AsnOctetString</b> structure to copy.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloctetsfree">SnmpUtilOctetsFree</a> function to free the memory that the 
<b>SnmpUtilOctetsCpy</b> function allocates for the destination structure.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloctetsfree">SnmpUtilOctetsFree</a>