---
UID: NF:winsnmp.SnmpCreatePdu
title: SnmpCreatePdu function (winsnmp.h)
description: The WinSNMP SnmpCreatePdu function creates and initializes an SNMP protocol data unit (PDU).
helpviewer_keywords: ["SNMP_PDU_GET","SNMP_PDU_GETBULK","SNMP_PDU_GETNEXT","SNMP_PDU_RESPONSE","SNMP_PDU_SET","SNMP_PDU_TRAP","SnmpCreatePdu","SnmpCreatePdu function [SNMP]","_snmp_snmpcreatepdu","snmp.snmpcreatepdu","winsnmp/SnmpCreatePdu"]
old-location: snmp\snmpcreatepdu.htm
tech.root: SNMP
ms.assetid: 1c73e8ab-ac66-43cd-8eec-e97dd3a98071
ms.date: 12/05/2018
ms.keywords: SNMP_PDU_GET, SNMP_PDU_GETBULK, SNMP_PDU_GETNEXT, SNMP_PDU_RESPONSE, SNMP_PDU_SET, SNMP_PDU_TRAP, SnmpCreatePdu, SnmpCreatePdu function [SNMP], _snmp_snmpcreatepdu, snmp.snmpcreatepdu, winsnmp/SnmpCreatePdu
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
 - SnmpCreatePdu
 - winsnmp/SnmpCreatePdu
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
 - SnmpCreatePdu
---

# SnmpCreatePdu function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpCreatePdu</b> function creates and initializes an SNMP protocol data unit (PDU).

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param PDU_type [in]

Specifies a PDU type that identifies the SNMP operation. This parameter can be <b>NULL</b>, or it can be one of the following values. If this parameter is <b>NULL</b>, the Microsoft WinSNMP implementation supplies the default PDU type SNMP_PDU_GETNEXT. The only type of trap PDU you can create with a call to the 
<b>SnmpCreatePdu</b> function is an SNMPv2C trap PDU. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_GET"></a><a id="snmp_pdu_get"></a><dl>
<dt><b>SNMP_PDU_GET</b></dt>
</dl>
</td>
<td width="60%">
Search and retrieve a value from a specified SNMP variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_GETNEXT"></a><a id="snmp_pdu_getnext"></a><dl>
<dt><b>SNMP_PDU_GETNEXT</b></dt>
</dl>
</td>
<td width="60%">
Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_RESPONSE"></a><a id="snmp_pdu_response"></a><dl>
<dt><b>SNMP_PDU_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Reply to an SNMP_PDU_GET or an SNMP_PDU_GETNEXT request.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_SET"></a><a id="snmp_pdu_set"></a><dl>
<dt><b>SNMP_PDU_SET</b></dt>
</dl>
</td>
<td width="60%">
Store a value in a specified SNMP variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_GETBULK"></a><a id="snmp_pdu_getbulk"></a><dl>
<dt><b>SNMP_PDU_GETBULK</b></dt>
</dl>
</td>
<td width="60%">
Search and retrieve multiple values with a single request.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_TRAP"></a><a id="snmp_pdu_trap"></a><dl>
<dt><b>SNMP_PDU_TRAP</b></dt>
</dl>
</td>
<td width="60%">
Alerts the management system to an event under SNMPv2C.

</td>
</tr>
</table>

### -param request_id [in]

Specifies a unique numeric value that the WinSNMP application supplies to identify the PDU. If this parameter is <b>NULL</b>, the implementation assigns a value.

### -param error_status [in]

If the <i>PDU_type</i> parameter is equal to <b>SNMP_PDU_GETBULK</b>, this parameter specifies a value for the <b>non_repeaters</b> field of the PDU. For other PDU types, this parameter specifies a value for the <b>error_status</b> field of the PDU. This parameter can be <b>NULL</b>.

### -param error_index [in]

If the <i>PDU_type</i> parameter is equal to <b>SNMP_PDU_GETBULK</b>, this parameter specifies a value for the <b>max_repetitions</b> field of the PDU. For other PDU types, this parameter specifies a value for the <b>error_index</b> field of the PDU. This parameter can be <b>NULL</b>.

### -param varbindlist [in]

Handle to a structure that represents an SNMP variable bindings list. This parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is the handle to a new SNMP PDU.

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
<dt><b>SNMPAPI_SESSION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The session handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The PDU type is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_VBL_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The variable bindings list is invalid.

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

A WinSNMP application must create a PDU before it calls the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> or the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a> functions.

All of the parameters of the 
<b>SnmpCreatePdu</b> function are required. However, all parameters, except the <i>session</i> parameter, can be <b>NULL</b>. In this instance, the new PDU has the following default values.

<table>
<tr>
<th>Field</th>
<th>Contents</th>
</tr>
<tr>
<td><b>PDU_type</b></td>
<td><b>SNMP_PDU_GETNEXT</b></td>
</tr>
<tr>
<td><b>request_id</b></td>
<td>The implementation generates a numeric value.</td>
</tr>
<tr>
<td><b>error_status</b></td>
<td>SNMP_ERROR_NOERROR</td>
</tr>
<tr>
<td><b>error_index</b></td>
<td>0</td>
</tr>
<tr>
<td><b>varbindlist</b></td>
<td><b>NULL</b></td>
</tr>
</table>
 

The application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a> function to release the resources that the 
<b>SnmpCreatePdu</b> function allocates for the new PDU.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>