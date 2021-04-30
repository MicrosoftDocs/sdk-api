---
UID: NF:winsnmp.SnmpOidToStr
title: SnmpOidToStr function (winsnmp.h)
description: The WinSNMP SnmpOidToStr function converts the internal binary representation of an SNMP object identifier to its dotted numeric string format, for example, to &quot;1.2.3.4.5.6&quot;.
helpviewer_keywords: ["SnmpOidToStr","SnmpOidToStr function [SNMP]","_snmp_snmpoidtostr","snmp.snmpoidtostr","winsnmp/SnmpOidToStr"]
old-location: snmp\snmpoidtostr.htm
tech.root: SNMP
ms.assetid: 20f0af32-8f4f-4326-ab6a-389dc95be73f
ms.date: 12/05/2018
ms.keywords: SnmpOidToStr, SnmpOidToStr function [SNMP], _snmp_snmpoidtostr, snmp.snmpoidtostr, winsnmp/SnmpOidToStr
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
 - SnmpOidToStr
 - winsnmp/SnmpOidToStr
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
 - SnmpOidToStr
---

# SnmpOidToStr function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpOidToStr</b> function converts the internal binary representation of an SNMP object identifier to its dotted numeric string format, for example, to "1.2.3.4.5.6".

## -parameters

### -param srcOID [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure with an object identifier to convert.

### -param size [in]

Specifies the size, in bytes, of the buffer indicated by the <i>string</i> parameter. For more information, see the following Remarks section.

### -param string [out]

Pointer to a buffer to receive the converted string object identifier that specifies the SNMP management entity.

## -returns

If the function succeeds, the return value is the length, in bytes, of the string that the WinSNMP application writes to the <i>string</i> parameter. The return value includes a <b>null</b>-terminating byte. This value may be less than or equal to the value of the <i>size</i> parameter, but it may not be greater.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
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
<dt><b>SNMPAPI_SIZE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>size</i> parameter is invalid. This parameter cannot be equal to zero; it must indicate the size of the buffer pointed to by the <i>string</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>srcOID</i> parameter is invalid. For additional information, see the following Remarks section.

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

It is recommended that a WinSNMP application specify, with the <i>size</i> parameter, a string buffer of MAXOBJIDSTRSIZE length (1408 bytes). This ensures that the output buffer is large enough to hold the converted string. Because the converted string is usually less than MAXOBJIDSTRSIZE, the WinSNMP application can copy the converted string to a smaller buffer. The application can then reuse or free the memory that it allocated for the initial buffer. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtooid">SnmpStrToOid</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a>