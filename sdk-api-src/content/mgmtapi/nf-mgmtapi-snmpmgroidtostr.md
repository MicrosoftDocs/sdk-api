---
UID: NF:mgmtapi.SnmpMgrOidToStr
title: SnmpMgrOidToStr function (mgmtapi.h)
description: The SnmpMgrOidToStr function converts an internal object identifier structure to its string representation. This function is an element of the SNMP Management API.
helpviewer_keywords: ["SnmpMgrOidToStr","SnmpMgrOidToStr function [SNMP]","_snmp_snmpmgroidtostr","mgmtapi/SnmpMgrOidToStr","snmp.snmpmgroidtostr"]
old-location: snmp\snmpmgroidtostr.htm
tech.root: SNMP
ms.assetid: 4864b864-3381-4129-8cc3-ecfc6566e530
ms.date: 12/05/2018
ms.keywords: SnmpMgrOidToStr, SnmpMgrOidToStr function [SNMP], _snmp_snmpmgroidtostr, mgmtapi/SnmpMgrOidToStr, snmp.snmpmgroidtostr
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
 - SnmpMgrOidToStr
 - mgmtapi/SnmpMgrOidToStr
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
 - SnmpMgrOidToStr
---

# SnmpMgrOidToStr function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrOidToStr</b> function converts an internal object identifier structure to its string representation. This function is an element of the SNMP Management API.

## -parameters

### -param oid [in]

Pointer to an object identifier variable to convert.

### -param string [out]

Pointer to a null-terminated string to receive the converted value.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

If the function succeeds, call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a> function to free the memory allocated for the converted string.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrstrtooid">SnmpMgrStrToOid</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a>