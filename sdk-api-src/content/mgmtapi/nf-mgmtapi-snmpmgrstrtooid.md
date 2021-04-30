---
UID: NF:mgmtapi.SnmpMgrStrToOid
title: SnmpMgrStrToOid function (mgmtapi.h)
description: The SnmpMgrStrToOid function converts the string format of an object identifier to its internal object identifier structure. This function is an element of the SNMP Management API.
helpviewer_keywords: ["SnmpMgrStrToOid","SnmpMgrStrToOid function [SNMP]","_snmp_snmpmgrstrtooid","mgmtapi/SnmpMgrStrToOid","snmp.snmpmgrstrtooid"]
old-location: snmp\snmpmgrstrtooid.htm
tech.root: SNMP
ms.assetid: d245b43c-3893-4081-874c-93619a8c461c
ms.date: 12/05/2018
ms.keywords: SnmpMgrStrToOid, SnmpMgrStrToOid function [SNMP], _snmp_snmpmgrstrtooid, mgmtapi/SnmpMgrStrToOid, snmp.snmpmgrstrtooid
req.header: mgmtapi.h
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
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpMgrStrToOid
 - mgmtapi/SnmpMgrStrToOid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mgmtapi.dll
api_name:
 - SnmpMgrStrToOid
---

# SnmpMgrStrToOid function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrStrToOid</b> function converts the string format of an object identifier to its internal object identifier structure. This function is an element of the SNMP Management API.

## -parameters

### -param string [in]

Pointer to a null-terminated string to convert.

### -param oid [out]

Pointer to an object identifier variable to receive the converted value.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

If the function succeeds, call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidfree">SnmpUtilOidFree</a> function to free the memory allocated for the converted object identifier.

If an application passes a valid object identifier to 
<b>SnmpMgrStrToOid</b>, yet is unable to obtain the requested variable, then the syntax of the system group and object identifier is incorrect. This occurs because 
<b>SnmpMgrStrToOid</b> assumes that the object identifier is under the Internet MIB of the management subtree.

You must always precede the object identifier with a period (.) to obtain the correct system group (for example, ".1.3.6.1.2.1.1"). If an application passes the variable "1.3.6.1.2.1.1", 
<b>SnmpMgrStrToOid</b> cannot interpret the object identifier correctly.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgroidtostr">SnmpMgrOidToStr</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidfree">SnmpUtilOidFree</a>