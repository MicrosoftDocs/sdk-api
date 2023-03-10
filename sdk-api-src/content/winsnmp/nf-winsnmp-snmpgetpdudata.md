---
UID: NF:winsnmp.SnmpGetPduData
title: SnmpGetPduData function (winsnmp.h)
description: The WinSNMP SnmpGetPduData function returns selected data fields from a specified SNMP protocol data unit (PDU).
helpviewer_keywords: ["SNMP_ERROR_AUTHORIZATIONERROR","SNMP_ERROR_BADVALUE","SNMP_ERROR_COMMITFAILED","SNMP_ERROR_GENERR","SNMP_ERROR_INCONSISTENTNAME","SNMP_ERROR_INCONSISTENTVALUE","SNMP_ERROR_NOACCESS","SNMP_ERROR_NOCREATION","SNMP_ERROR_NOERROR","SNMP_ERROR_NOSUCHNAME","SNMP_ERROR_NOTWRITABLE","SNMP_ERROR_READONLY","SNMP_ERROR_RESOURCEUNAVAILABLE","SNMP_ERROR_TOOBIG","SNMP_ERROR_UNDOFAILED","SNMP_ERROR_WRONGENCODING","SNMP_ERROR_WRONGLENGTH","SNMP_ERROR_WRONGTYPE","SNMP_ERROR_WRONGVALUE","SNMP_PDU_GET","SNMP_PDU_GETBULK","SNMP_PDU_GETNEXT","SNMP_PDU_RESPONSE","SNMP_PDU_SET","SNMP_PDU_TRAP","SnmpGetPduData","SnmpGetPduData function [SNMP]","_snmp_snmpgetpdudata","snmp.snmpgetpdudata","winsnmp/SnmpGetPduData"]
old-location: snmp\snmpgetpdudata.htm
tech.root: SNMP
ms.assetid: 5dff1bc0-aac4-490f-aef0-11d090567761
ms.date: 12/05/2018
ms.keywords: SNMP_ERROR_AUTHORIZATIONERROR, SNMP_ERROR_BADVALUE, SNMP_ERROR_COMMITFAILED, SNMP_ERROR_GENERR, SNMP_ERROR_INCONSISTENTNAME, SNMP_ERROR_INCONSISTENTVALUE, SNMP_ERROR_NOACCESS, SNMP_ERROR_NOCREATION, SNMP_ERROR_NOERROR, SNMP_ERROR_NOSUCHNAME, SNMP_ERROR_NOTWRITABLE, SNMP_ERROR_READONLY, SNMP_ERROR_RESOURCEUNAVAILABLE, SNMP_ERROR_TOOBIG, SNMP_ERROR_UNDOFAILED, SNMP_ERROR_WRONGENCODING, SNMP_ERROR_WRONGLENGTH, SNMP_ERROR_WRONGTYPE, SNMP_ERROR_WRONGVALUE, SNMP_PDU_GET, SNMP_PDU_GETBULK, SNMP_PDU_GETNEXT, SNMP_PDU_RESPONSE, SNMP_PDU_SET, SNMP_PDU_TRAP, SnmpGetPduData, SnmpGetPduData function [SNMP], _snmp_snmpgetpdudata, snmp.snmpgetpdudata, winsnmp/SnmpGetPduData
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
 - SnmpGetPduData
 - winsnmp/SnmpGetPduData
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
 - SnmpGetPduData
---

# SnmpGetPduData function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpGetPduData</b> function returns selected data fields from a specified SNMP protocol data unit (PDU).

## -parameters

### -param PDU [in]

Handle to the SNMP PDU.

### -param PDU_type [out]

Pointer to a variable that receives the <b>PDU_type</b> field of the specified PDU. This parameter can be <b>NULL</b>, or one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_GET_"></a><a id="snmp_pdu_get_"></a><dl>
<dt><b>SNMP_PDU_GET </b></dt>
</dl>
</td>
<td width="60%">
Search and retrieve a value from a specified SNMP variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_GETNEXT_"></a><a id="snmp_pdu_getnext_"></a><dl>
<dt><b>SNMP_PDU_GETNEXT </b></dt>
</dl>
</td>
<td width="60%">
Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_RESPONSE_"></a><a id="snmp_pdu_response_"></a><dl>
<dt><b>SNMP_PDU_RESPONSE </b></dt>
</dl>
</td>
<td width="60%">
Reply to an <b>SNMP_PDU_GET</b> or an <b>SNMP_PDU_GETNEXT</b> request.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_SET_"></a><a id="snmp_pdu_set_"></a><dl>
<dt><b>SNMP_PDU_SET </b></dt>
</dl>
</td>
<td width="60%">
Store a value in a specified SNMP variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_GETBULK_"></a><a id="snmp_pdu_getbulk_"></a><dl>
<dt><b>SNMP_PDU_GETBULK </b></dt>
</dl>
</td>
<td width="60%">
Search and retrieve multiple values with a single request.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_TRAP_"></a><a id="snmp_pdu_trap_"></a><dl>
<dt><b>SNMP_PDU_TRAP </b></dt>
</dl>
</td>
<td width="60%">
Alerts the management system to an extraordinary event under SNMPv2C.

</td>
</tr>
</table>

### -param request_id [out]

Pointer to a variable that receives the <b>request_id</b> field of the specified PDU. This parameter can be <b>NULL</b>.

### -param error_status [out]

Pointer to a variable that receives the <b>error_status</b> field of the specified PDU. If the <i>PDU_type</i> parameter is equal to <b>SNMP_PDU_GETBULK</b>, this parameter receives the value of the <b>non_repeaters</b> field of the PDU. 




This parameter can be <b>NULL</b>, or one of the following values. The first six errors are common to the SNMP version 1 (SNMPv1) and SNMP version 2C frameworks (SNMPv2C). The remaining errors are available under SNMPv2C only.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_NOERROR"></a><a id="snmp_error_noerror"></a><dl>
<dt><b>SNMP_ERROR_NOERROR</b></dt>
</dl>
</td>
<td width="60%">
The agent reports that no errors occurred during transmission.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_TOOBIG"></a><a id="snmp_error_toobig"></a><dl>
<dt><b>SNMP_ERROR_TOOBIG</b></dt>
</dl>
</td>
<td width="60%">
The agent could not place the results of the requested SNMP operation into a single SNMP message.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_NOSUCHNAME"></a><a id="snmp_error_nosuchname"></a><dl>
<dt><b>SNMP_ERROR_NOSUCHNAME</b></dt>
</dl>
</td>
<td width="60%">
The requested SNMP operation identified an unknown variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_BADVALUE"></a><a id="snmp_error_badvalue"></a><dl>
<dt><b>SNMP_ERROR_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
The requested SNMP operation tried to change a variable but it specified either a syntax or value error.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_READONLY"></a><a id="snmp_error_readonly"></a><dl>
<dt><b>SNMP_ERROR_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The requested SNMP operation tried to change a variable that was not allowed to change, according to the community profile of the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_GENERR"></a><a id="snmp_error_generr"></a><dl>
<dt><b>SNMP_ERROR_GENERR</b></dt>
</dl>
</td>
<td width="60%">
An error other than one of those listed here occurred during the requested SNMP operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_NOACCESS"></a><a id="snmp_error_noaccess"></a><dl>
<dt><b>SNMP_ERROR_NOACCESS</b></dt>
</dl>
</td>
<td width="60%">
The specified SNMP variable is not accessible.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_WRONGTYPE"></a><a id="snmp_error_wrongtype"></a><dl>
<dt><b>SNMP_ERROR_WRONGTYPE</b></dt>
</dl>
</td>
<td width="60%">
The value specifies a type that is inconsistent with the type required for the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_WRONGLENGTH"></a><a id="snmp_error_wronglength"></a><dl>
<dt><b>SNMP_ERROR_WRONGLENGTH</b></dt>
</dl>
</td>
<td width="60%">
The value specifies a length that is inconsistent with the length required for the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_WRONGENCODING"></a><a id="snmp_error_wrongencoding"></a><dl>
<dt><b>SNMP_ERROR_WRONGENCODING</b></dt>
</dl>
</td>
<td width="60%">
The value contains an Abstract Syntax Notation One (ASN.1) encoding that is inconsistent with the ASN.1 tag of the field.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_WRONGVALUE"></a><a id="snmp_error_wrongvalue"></a><dl>
<dt><b>SNMP_ERROR_WRONGVALUE</b></dt>
</dl>
</td>
<td width="60%">
The value cannot be assigned to the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_NOCREATION"></a><a id="snmp_error_nocreation"></a><dl>
<dt><b>SNMP_ERROR_NOCREATION</b></dt>
</dl>
</td>
<td width="60%">
The variable does not exist, and the agent cannot create it.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_INCONSISTENTVALUE"></a><a id="snmp_error_inconsistentvalue"></a><dl>
<dt><b>SNMP_ERROR_INCONSISTENTVALUE</b></dt>
</dl>
</td>
<td width="60%">
The value is inconsistent with values of other managed objects.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_RESOURCEUNAVAILABLE"></a><a id="snmp_error_resourceunavailable"></a><dl>
<dt><b>SNMP_ERROR_RESOURCEUNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
Assigning the value to the variable requires allocation of resources that are currently unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_COMMITFAILED"></a><a id="snmp_error_commitfailed"></a><dl>
<dt><b>SNMP_ERROR_COMMITFAILED</b></dt>
</dl>
</td>
<td width="60%">
No validation errors occurred, but no variables were updated.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_UNDOFAILED"></a><a id="snmp_error_undofailed"></a><dl>
<dt><b>SNMP_ERROR_UNDOFAILED</b></dt>
</dl>
</td>
<td width="60%">
No validation errors occurred. Some variables were updated because it was not possible to undo their assignment.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_AUTHORIZATIONERROR"></a><a id="snmp_error_authorizationerror"></a><dl>
<dt><b>SNMP_ERROR_AUTHORIZATIONERROR</b></dt>
</dl>
</td>
<td width="60%">
An authorization error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_NOTWRITABLE"></a><a id="snmp_error_notwritable"></a><dl>
<dt><b>SNMP_ERROR_NOTWRITABLE</b></dt>
</dl>
</td>
<td width="60%">
The variable exists but the agent cannot modify it.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERROR_INCONSISTENTNAME"></a><a id="snmp_error_inconsistentname"></a><dl>
<dt><b>SNMP_ERROR_INCONSISTENTNAME</b></dt>
</dl>
</td>
<td width="60%">
The variable does not exist; the agent cannot create it because the named object instance is inconsistent with the values of other managed objects.

</td>
</tr>
</table>

### -param error_index [out]

Pointer to a variable that receives the <b>error_index</b> field of the specified PDU. 




If the <i>PDU_type</i> parameter is equal to <b>SNMP_PDU_GETBULK</b>, this parameter receives the value of the <b>max_repetitions</b> field of the specified PDU. This parameter can be <b>NULL</b>.

### -param varbindlist [out]

Pointer to a variable that receives a handle to the variable bindings list field of the specified PDU. This parameter can be <b>NULL</b>. For additional information, see the following Remarks section.

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
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
All output parameters are <b>NULL</b>. The SNMP operation was not performed.

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
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>

## -remarks

All parameters of the 
<b>SnmpGetPduData</b> function are required. However, all parameters, except the <i>PDU</i> parameter, can be <b>NULL</b>. In parameters that the application passes as <b>NULL</b>, the 
<b>SnmpGetPduData</b> function does not return a value.

The 
<b>SnmpGetPduData</b> function always returns a handle to a new variable bindings list object if the <i>varbindlist</i> parameter is not <b>NULL</b>. Additionally, if the <i>PDU</i> parameter specifies a new PDU, the function also attaches a handle to the new PDU.

When an application calls 
<b>SnmpGetPduData</b> with a <i>varbindlist</i> parameter that is not <b>NULL</b>, but the <i>PDU</i> parameter specifies an existing PDU, the function returns a handle to a new duplicate variable bindings list. The function call does not disturb the handle attached to the existing PDU. An existing PDU is one that an application creates with a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatepdu">SnmpCreatePdu</a> function, or one that the application receives and then reads using a call to 
<b>SnmpGetPduData</b>.

When an application creates a PDU with 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatepdu">SnmpCreatePdu</a>, or after the application reads a PDU using 
<b>SnmpGetPduData</b>, the Microsoft WinSNMP implementation expects that the application "knows" the values of the PDU fields. If an application reads a PDU a second time with 
<b>SnmpGetPduData</b>, the call results in a copy of the variable bindings list of the specified PDU. This type of call to 
<b>SnmpGetPduData</b> also duplicates the handle to the PDU.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatepdu">SnmpCreatePdu</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatevbl">SnmpDuplicateVbl</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>