---
UID: NF:winsnmp.SnmpEntityToStr
title: SnmpEntityToStr function (winsnmp.h)
description: The WinSNMP SnmpEntityToStr function returns a string that identifies an SNMP management entity.
helpviewer_keywords: ["SnmpEntityToStr","SnmpEntityToStr function [SNMP]","_snmp_snmpentitytostr","snmp.snmpentitytostr","winsnmp/SnmpEntityToStr"]
old-location: snmp\snmpentitytostr.htm
tech.root: SNMP
ms.assetid: 3a5bca7e-a0a2-4bf5-86cc-f8d9f3ac8660
ms.date: 12/05/2018
ms.keywords: SnmpEntityToStr, SnmpEntityToStr function [SNMP], _snmp_snmpentitytostr, snmp.snmpentitytostr, winsnmp/SnmpEntityToStr
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
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpEntityToStr
 - winsnmp/SnmpEntityToStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpEntityToStr
---

# SnmpEntityToStr function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpEntityToStr</b> function returns a string that identifies an SNMP management entity.

## -parameters

### -param entity [in]

Handle to the SNMP management entity of interest.

### -param size [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>string</i> parameter. The WinSNMP application must allocate a buffer that is large enough to contain the output string.

### -param string [out]

Pointer to a buffer to receive the null-terminated string that identifies the SNMP management entity of interest.

## -returns

If the function succeeds, the return value is the number of bytes, including a terminating null byte, that 
<b>SnmpEntityToStr</b> returns in the <i>string</i> buffer. This value can be less than or equal to the value of the <i>size</i> parameter, but it cannot be greater.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a>. The 
<b>SnmpGetLastError</b> function can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>entity</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OUTPUT_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The output buffer length is insufficient.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>

## -remarks

The current setting of the entity and context translation mode determines the type of output string 
<b>SnmpEntityToStr</b> returns. For additional information, see 
<a href="/windows/desktop/SNMP/support-for-ipx-address-strings-in-winsnmp">Support for IPX Address Strings in WinSNMP</a> and 
<a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a>.

When the entity and context translation mode is SNMPAPI_TRANSLATED, and an entry exists in the implementation's database, the implementation returns the associated user-friendly name of the management entity. If an entry does not exist for the management entity, 
<b>SnmpEntityToStr</b> returns the literal SNMP transport address of the management entity.

When the entity and context translation mode is SNMPAPI_UNTRANSLATED_V1 or SNMPAPI_UNTRANSLATED_V2, the Microsoft WinSNMP implementation also returns the literal SNMP transport address of the management entity.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>