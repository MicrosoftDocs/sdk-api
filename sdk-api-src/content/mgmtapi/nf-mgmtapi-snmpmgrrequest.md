---
UID: NF:mgmtapi.SnmpMgrRequest
title: SnmpMgrRequest function (mgmtapi.h)
description: The SnmpMgrRequest function requests the specified operation be performed with the specified agent. This function is an element of the SNMP Management API.
helpviewer_keywords: ["SNMP_ERRORSTATUS_BADVALUE","SNMP_ERRORSTATUS_GENERR","SNMP_ERRORSTATUS_NOERROR","SNMP_ERRORSTATUS_NOSUCHNAME","SNMP_ERRORSTATUS_READONLY","SNMP_ERRORSTATUS_TOOBIG","SNMP_PDU_GET","SNMP_PDU_GETNEXT","SNMP_PDU_SET","SnmpMgrRequest","SnmpMgrRequest function [SNMP]","_snmp_snmpmgrrequest","mgmtapi/SnmpMgrRequest","snmp.snmpmgrrequest"]
old-location: snmp\snmpmgrrequest.htm
tech.root: SNMP
ms.assetid: f66ce774-dba0-466b-ad1e-671f9a487e0f
ms.date: 12/05/2018
ms.keywords: SNMP_ERRORSTATUS_BADVALUE, SNMP_ERRORSTATUS_GENERR, SNMP_ERRORSTATUS_NOERROR, SNMP_ERRORSTATUS_NOSUCHNAME, SNMP_ERRORSTATUS_READONLY, SNMP_ERRORSTATUS_TOOBIG, SNMP_PDU_GET, SNMP_PDU_GETNEXT, SNMP_PDU_SET, SnmpMgrRequest, SnmpMgrRequest function [SNMP], _snmp_snmpmgrrequest, mgmtapi/SnmpMgrRequest, snmp.snmpmgrrequest
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
 - SnmpMgrRequest
 - mgmtapi/SnmpMgrRequest
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
 - SnmpMgrRequest
---

# SnmpMgrRequest function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrRequest</b> function requests the specified operation be performed with the specified agent. This function is an element of the SNMP Management API.

## -parameters

### -param session [in]

Pointer to an internal structure that specifies the session that will perform the request. 




Applications should not specify the <b>LPSNMP_MGR_SESSION</b> pointer returned by this function in a different thread. You can specify a pointer returned by 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgropen">SnmpMgrOpen</a>, but only if the calls to 
<b>SnmpMgrOpen</b> and 
<b>SnmpMgrRequest</b> originate in the context of the same thread.

### -param requestType [in]

Specifies the SNMP request type. This parameter can be one of the following values defined by SNMPv1. 



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
Retrieve the value or values of the specified variables.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_GETNEXT"></a><a id="snmp_pdu_getnext"></a><dl>
<dt><b>SNMP_PDU_GETNEXT</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the value or values of the lexicographic successor of the specified variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_PDU_SET"></a><a id="snmp_pdu_set"></a><dl>
<dt><b>SNMP_PDU_SET</b></dt>
</dl>
</td>
<td width="60%">
Write a value within a specific variable.

</td>
</tr>
</table>
 

Note that PDU request types have been renamed. For additional information, see 
<a href="/windows/desktop/SNMP/snmp-variable-types-and-request-pdu-types">SNMP Variable Types and Request PDU Types</a>.

### -param variableBindings [in, out]

Pointer to the variable bindings list. 

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> array pointed to by the <a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure must be allocated using the <a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a> function.</div>
<div> </div>

### -param errorStatus [out]

Pointer to a variable in which the error status result will be returned. This parameter can be one of the following values defined by SNMPv1. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_NOERROR"></a><a id="snmp_errorstatus_noerror"></a><dl>
<dt><b>SNMP_ERRORSTATUS_NOERROR</b></dt>
</dl>
</td>
<td width="60%">
The agent reports that no errors occurred during transmission.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_TOOBIG"></a><a id="snmp_errorstatus_toobig"></a><dl>
<dt><b>SNMP_ERRORSTATUS_TOOBIG</b></dt>
</dl>
</td>
<td width="60%">
The agent could not place the results of the requested operation into a single SNMP message.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_NOSUCHNAME"></a><a id="snmp_errorstatus_nosuchname"></a><dl>
<dt><b>SNMP_ERRORSTATUS_NOSUCHNAME</b></dt>
</dl>
</td>
<td width="60%">
The requested operation identified an unknown variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_BADVALUE"></a><a id="snmp_errorstatus_badvalue"></a><dl>
<dt><b>SNMP_ERRORSTATUS_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation tried to change a variable but it specified either a syntax or value error.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_READONLY"></a><a id="snmp_errorstatus_readonly"></a><dl>
<dt><b>SNMP_ERRORSTATUS_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The requested operation tried to change a variable that was not allowed to change according to the community profile of the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_GENERR"></a><a id="snmp_errorstatus_generr"></a><dl>
<dt><b>SNMP_ERRORSTATUS_GENERR</b></dt>
</dl>
</td>
<td width="60%">
An error other than one of those listed here occurred during the requested operation.

</td>
</tr>
</table>

### -param errorIndex [out]

Pointer to a variable in which the error index result will be returned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which may return one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The request timed-out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_SELECT_FDERRORS</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error file descriptors indicated by the Windows Sockets 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> function.

</td>
</tr>
</table>

## -remarks

Retries and time-outs are supplied to the 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgropen">SnmpMgrOpen</a> function. Each variable in the variable bindings list must be initialized to type ASN_NULL for Get and Get Next requests.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrclose">SnmpMgrClose</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgropen">SnmpMgrOpen</a>