---
UID: NF:winsnmp.SnmpDeleteVb
title: SnmpDeleteVb function (winsnmp.h)
description: The WinSNMP SnmpDeleteVb function removes a variable binding entry from a variable bindings list.
helpviewer_keywords: ["SnmpDeleteVb","SnmpDeleteVb function [SNMP]","_snmp_snmpdeletevb","snmp.snmpdeletevb","winsnmp/SnmpDeleteVb"]
old-location: snmp\snmpdeletevb.htm
tech.root: SNMP
ms.assetid: b6f8a61a-493c-4626-9134-f8badce678c4
ms.date: 12/05/2018
ms.keywords: SnmpDeleteVb, SnmpDeleteVb function [SNMP], _snmp_snmpdeletevb, snmp.snmpdeletevb, winsnmp/SnmpDeleteVb
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
 - SnmpDeleteVb
 - winsnmp/SnmpDeleteVb
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
 - SnmpDeleteVb
---

# SnmpDeleteVb function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpDeleteVb</b> function removes a variable binding entry from a variable bindings list.

## -parameters

### -param vbl [in]

Handle to the variable bindings list to update.

### -param index [in]

Specifies an unsigned long integer variable that identifies the variable binding entry to remove. This variable contains the position of the variable binding entry, within the variable bindings list. 




Valid values for this parameter are in the range from 1 to n, where 1 indicates the first variable binding entry in the variable bindings list, and n is the total number of entries in the variable bindings list. For additional information, see the following Remarks section.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

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
<dt><b>SNMPAPI_INDEX_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_VBL_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>vbl</i> parameter is invalid.

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

A WinSNMP application can use the 
<b>SnmpDeleteVb</b> function to delete invalid variable binding entries. When an <a href="/windows/desktop/SNMP/snmp-variable-types-and-request-pdu-types">SNMP_PDU_RESPONSE</a> protocol data unit (PDU) includes an error that indicates an invalid variable binding entry, the application can call 
<b>SnmpDeleteVb</b> to delete the entry. Then the application can resubmit the request PDU with a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function, without the invalid variable binding entry in the variable bindings list. Request PDUs include the SNMP_PDU_GET, SNMP_PDU_GETNEXT, and SNMP_PDU_GETBULK PDU data types.

After the 
<b>SnmpDeleteVb</b> function deletes a variable binding entry, the index value of all entries after the deleted entry will decrement by one. A call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcountvbl">SnmpCountVbl</a> function returns the new total number of entries in the variable bindings list. The new total is one less than the count returned by a call to 
<b>SnmpCountVbl</b> before the current call to 
<b>SnmpDeleteVb</b>.

If a WinSNMP application calls the 
<b>SnmpDeleteVb</b> function and deletes the last variable binding entry in a variable bindings list, the result is an empty variable bindings list. The variable bindings list still has a valid handle and the WinSNMP application must release the handle with a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a> function.

The following are valid values to use for the <i>index</i> parameter:

<ul>
<li>The return value from a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcountvbl">SnmpCountVbl</a> function</li>
<li>The error index field of an <a href="/windows/desktop/SNMP/snmp-variable-types-and-request-pdu-types">SNMP_PDU_RESPONSE</a> PDU returned by a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a> function</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcountvbl">SnmpCountVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>