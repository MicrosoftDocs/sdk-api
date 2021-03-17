---
UID: NF:snmp.SnmpExtensionQuery
title: SnmpExtensionQuery function (snmp.h)
description: The Microsoft SNMP service calls the SnmpExtensionQuery function to resolve SNMP requests that contain variables within one or more of the SNMP extension agent's registered MIB subtrees. This function is an element of the SNMP Extension Agent API.
helpviewer_keywords: ["SNMP_ERRORSTATUS_BADVALUE","SNMP_ERRORSTATUS_GENERR","SNMP_ERRORSTATUS_NOERROR","SNMP_ERRORSTATUS_NOSUCHNAME","SNMP_ERRORSTATUS_READONLY","SNMP_ERRORSTATUS_TOOBIG","SNMP_PDU_GET","SNMP_PDU_GETNEXT","SNMP_PDU_SET","SnmpExtensionQuery","SnmpExtensionQuery callback","SnmpExtensionQuery callback function [SNMP]","_snmp_snmpextensionquery","snmp.snmpextensionquery","snmp/SnmpExtensionQuery"]
old-location: snmp\snmpextensionquery.htm
tech.root: SNMP
ms.assetid: 5ca25e1d-d0aa-490e-a591-57b25a77b1da
ms.date: 12/05/2018
ms.keywords: SNMP_ERRORSTATUS_BADVALUE, SNMP_ERRORSTATUS_GENERR, SNMP_ERRORSTATUS_NOERROR, SNMP_ERRORSTATUS_NOSUCHNAME, SNMP_ERRORSTATUS_READONLY, SNMP_ERRORSTATUS_TOOBIG, SNMP_PDU_GET, SNMP_PDU_GETNEXT, SNMP_PDU_SET, SnmpExtensionQuery, SnmpExtensionQuery callback, SnmpExtensionQuery callback function [SNMP], _snmp_snmpextensionquery, snmp.snmpextensionquery, snmp/SnmpExtensionQuery
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpExtensionQuery
 - snmp/SnmpExtensionQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Snmp.h
api_name:
 - SnmpExtensionQuery
---

# SnmpExtensionQuery function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionQuery</b> function to resolve SNMP requests that contain variables within one or more of the SNMP extension agent's registered MIB subtrees. This function is an element of the SNMP Extension Agent API.
<div class="alert"><b>Note</b>  It is recommended that you use the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionqueryex">SnmpExtensionQueryEx</a> function, which supports SNMP version 2C (SNMPv2C) data types and multiphase SNMP SET operations.</div><div> </div>

## -parameters

### -param bPduType [in]

Specifies the SNMP version 1 (SNMPv1) PDU request type. This parameter can be one of the following values. 



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

### -param pVarBindList [in, out]

Pointer to the variable bindings list.

### -param pErrorStatus [out]

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

### -param pErrorIndex [out]

Pointer to a variable in which the error index result will be returned.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

When the SNMP service receives an SNMP PDU request, it calls the 
<b>SnmpExtensionQuery</b> function to process the request. The extension agent must follow the rules in RFC 1157 to either resolve the variable bindings or generate an error.

If the extension agent cannot resolve the variable bindings on a <b>Get Next</b> request, it must change the <b>name</b> field of the 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure to the value of the object identifier immediately following that of the currently supported MIB subtree view. For example, if the extension agent supports view ".1.3.6.1.4.1.77.1", a <b>Get Next</b> request on ".1.3.6.1.4.1.77.1.5.1" would result in a modified <b>name</b> field of ".1.3.6.1.4.1.77.2". This signals the SNMP service to continue the attempt to resolve the variable bindings with other extension agents.

It is important to note that the SNMP service and the extension agent may need to exchange dynamically allocated memory during a call to the 
<b>SnmpExtensionQuery</b> function. The service dynamically allocates the object identifier in each 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure it passes to the extension agent. However, the extension agent must release this memory in order to replace the object identifier when it processes a <b>Get Next</b> request. The extension agent allocates dynamic memory for variable-length object types. The SNMP service releases this memory after the object is placed in the response PDU.

In order to avoid heap corruption and memory leaks, both the SNMP service and the extension agent must use memory allocation routines that resolve to the same heap. The extension agent must use the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a> function to allocate memory that it passes to the SNMP service. It must use the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a> function to release the memory the service passes back to the extension agent. These functions are located in the utility dynamic-link library SNMPAPI.DLL.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a>