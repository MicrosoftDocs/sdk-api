---
UID: NF:snmp.SnmpExtensionQueryEx
title: SnmpExtensionQueryEx function (snmp.h)
description: The Microsoft SNMP service calls the SnmpExtensionQueryEx function to process SNMP requests that specify variables in one or more MIB subtrees registered by SNMP extension agents. This function is an element of the SNMP Extension Agent API.
helpviewer_keywords: ["SNMP_ERRORSTATUS_AUTHORIZATIONERROR","SNMP_ERRORSTATUS_BADVALUE","SNMP_ERRORSTATUS_COMMITFAILED","SNMP_ERRORSTATUS_GENERR","SNMP_ERRORSTATUS_INCONSISTENTNAME","SNMP_ERRORSTATUS_INCONSISTENTVALUE","SNMP_ERRORSTATUS_NOACCESS","SNMP_ERRORSTATUS_NOCREATION","SNMP_ERRORSTATUS_NOERROR","SNMP_ERRORSTATUS_NOSUCHNAME","SNMP_ERRORSTATUS_NOTWRITABLE","SNMP_ERRORSTATUS_READONLY","SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE","SNMP_ERRORSTATUS_TOOBIG","SNMP_ERRORSTATUS_UNDOFAILED","SNMP_ERRORSTATUS_WRONGENCODING","SNMP_ERRORSTATUS_WRONGLENGTH","SNMP_ERRORSTATUS_WRONGTYPE","SNMP_ERRORSTATUS_WRONGVALUE","SNMP_EXTENSION_GET","SNMP_EXTENSION_GET_NEXT","SNMP_EXTENSION_SET_CLEANUP","SNMP_EXTENSION_SET_COMMIT","SNMP_EXTENSION_SET_TEST","SNMP_EXTENSION_SET_UNDO","SnmpExtensionQueryEx","SnmpExtensionQueryEx callback","SnmpExtensionQueryEx callback function [SNMP]","_snmp_snmpextensionqueryex","snmp.snmpextensionqueryex","snmp/SnmpExtensionQueryEx"]
old-location: snmp\snmpextensionqueryex.htm
tech.root: SNMP
ms.assetid: 2479c6ea-93f8-4b23-a0b7-645bf27f252f
ms.date: 12/05/2018
ms.keywords: SNMP_ERRORSTATUS_AUTHORIZATIONERROR, SNMP_ERRORSTATUS_BADVALUE, SNMP_ERRORSTATUS_COMMITFAILED, SNMP_ERRORSTATUS_GENERR, SNMP_ERRORSTATUS_INCONSISTENTNAME, SNMP_ERRORSTATUS_INCONSISTENTVALUE, SNMP_ERRORSTATUS_NOACCESS, SNMP_ERRORSTATUS_NOCREATION, SNMP_ERRORSTATUS_NOERROR, SNMP_ERRORSTATUS_NOSUCHNAME, SNMP_ERRORSTATUS_NOTWRITABLE, SNMP_ERRORSTATUS_READONLY, SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE, SNMP_ERRORSTATUS_TOOBIG, SNMP_ERRORSTATUS_UNDOFAILED, SNMP_ERRORSTATUS_WRONGENCODING, SNMP_ERRORSTATUS_WRONGLENGTH, SNMP_ERRORSTATUS_WRONGTYPE, SNMP_ERRORSTATUS_WRONGVALUE, SNMP_EXTENSION_GET, SNMP_EXTENSION_GET_NEXT, SNMP_EXTENSION_SET_CLEANUP, SNMP_EXTENSION_SET_COMMIT, SNMP_EXTENSION_SET_TEST, SNMP_EXTENSION_SET_UNDO, SnmpExtensionQueryEx, SnmpExtensionQueryEx callback, SnmpExtensionQueryEx callback function [SNMP], _snmp_snmpextensionqueryex, snmp.snmpextensionqueryex, snmp/SnmpExtensionQueryEx
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
 - SnmpExtensionQueryEx
 - snmp/SnmpExtensionQueryEx
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
 - SnmpExtensionQueryEx
---

# SnmpExtensionQueryEx function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionQueryEx</b> function to process SNMP requests that specify variables in one or more MIB subtrees registered by SNMP extension agents. This function is an element of the SNMP Extension Agent API.
<div class="alert"><b>Note</b>  It is recommended that you use the 
<b>SnmpExtensionQueryEx</b> function, which supports SNMP version 2C (SNMPv2C) data types and multiphase SNMP SET operations. The SNMP service does not call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionquery">SnmpExtensionQuery</a> function if the extension agent exports the 
<b>SnmpExtensionQueryEx</b> function.</div><div> </div>

## -parameters

### -param nRequestType [in]

Specifies the type of operation that the SNMP service is requesting the extension agent to perform. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXTENSION_GET"></a><a id="snmp_extension_get"></a><dl>
<dt><b>SNMP_EXTENSION_GET</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the value or values of the specified variables.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXTENSION_GET_NEXT"></a><a id="snmp_extension_get_next"></a><dl>
<dt><b>SNMP_EXTENSION_GET_NEXT</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the value or values of the lexicographic successor of the specified variables.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXTENSION_SET_TEST"></a><a id="snmp_extension_set_test"></a><dl>
<dt><b>SNMP_EXTENSION_SET_TEST</b></dt>
</dl>
</td>
<td width="60%">
Validate the values of the specified variables. This operation maximizes the probability of a successful write during the 
COMMIT request.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXTENSION_SET_COMMIT"></a><a id="snmp_extension_set_commit"></a><dl>
<dt><b>SNMP_EXTENSION_SET_COMMIT</b></dt>
</dl>
</td>
<td width="60%">
Write the new values to the specified variables.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXTENSION_SET_UNDO"></a><a id="snmp_extension_set_undo"></a><dl>
<dt><b>SNMP_EXTENSION_SET_UNDO</b></dt>
</dl>
</td>
<td width="60%">
Reset the values of the specified variables to their values before the COMMIT request.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXTENSION_SET_CLEANUP"></a><a id="snmp_extension_set_cleanup"></a><dl>
<dt><b>SNMP_EXTENSION_SET_CLEANUP</b></dt>
</dl>
</td>
<td width="60%">
Release the resources allocated in previous requests and operations.

</td>
</tr>
</table>
 

For additional information about the SET request types, that is, those that begin with SNMP_EXTENSION_SET_, see the following Remarks section.

### -param nTransactionId [in]

Specifies a <b>DWORD</b> variable that is the unique identifier of the incoming SNMP request PDU. The extension agent can use this value to correlate multiple calls by the SNMP service that involve the same PDU.

### -param pVarBindList [in, out]

Pointer to the variable binding list containing the variables of interest.

### -param pContextInfo [in, out]

Pointer to an octet string that contains user-defined context information. 




The extension agent can use this parameter to store context information used during multiphase SNMP SET operations. The extension agent must release resources associated with this parameter during the 
CLEANUP request. The SNMP service does not release any resources associated with this parameter. For additional information, see the following Remarks section.

### -param pErrorStatus [out]

Pointer to a variable to receive the error status result. This parameter can be one of the following values defined by SNMPv2C. 



<table>
<tr>
<th>Error code</th>
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
The agent could not place the results of the requested SNMP operation into a single SNMP message.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_NOSUCHNAME"></a><a id="snmp_errorstatus_nosuchname"></a><dl>
<dt><b>SNMP_ERRORSTATUS_NOSUCHNAME</b></dt>
</dl>
</td>
<td width="60%">
The requested SNMP operation identified an unknown variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_BADVALUE"></a><a id="snmp_errorstatus_badvalue"></a><dl>
<dt><b>SNMP_ERRORSTATUS_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
The requested SNMP operation tried to change a variable but it specified either a syntax or value error.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_READONLY"></a><a id="snmp_errorstatus_readonly"></a><dl>
<dt><b>SNMP_ERRORSTATUS_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The requested SNMP operation tried to change a variable that was not allowed to change, according to the community profile of the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_GENERR"></a><a id="snmp_errorstatus_generr"></a><dl>
<dt><b>SNMP_ERRORSTATUS_GENERR</b></dt>
</dl>
</td>
<td width="60%">
An error other than one of those listed here occurred during the requested SNMP operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_NOACCESS"></a><a id="snmp_errorstatus_noaccess"></a><dl>
<dt><b>SNMP_ERRORSTATUS_NOACCESS</b></dt>
</dl>
</td>
<td width="60%">
The specified SNMP variable is not accessible.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_WRONGTYPE"></a><a id="snmp_errorstatus_wrongtype"></a><dl>
<dt><b>SNMP_ERRORSTATUS_WRONGTYPE</b></dt>
</dl>
</td>
<td width="60%">
The value specifies a type that is inconsistent with the type required for the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_WRONGLENGTH"></a><a id="snmp_errorstatus_wronglength"></a><dl>
<dt><b>SNMP_ERRORSTATUS_WRONGLENGTH</b></dt>
</dl>
</td>
<td width="60%">
The value specifies a length that is inconsistent with the length required for the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_WRONGENCODING"></a><a id="snmp_errorstatus_wrongencoding"></a><dl>
<dt><b>SNMP_ERRORSTATUS_WRONGENCODING</b></dt>
</dl>
</td>
<td width="60%">
The value contains an Abstract Syntax Notation One (ASN.1) encoding that is inconsistent with the ASN.1 tag of the field.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_WRONGVALUE"></a><a id="snmp_errorstatus_wrongvalue"></a><dl>
<dt><b>SNMP_ERRORSTATUS_WRONGVALUE</b></dt>
</dl>
</td>
<td width="60%">
The value cannot be assigned to the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_NOCREATION"></a><a id="snmp_errorstatus_nocreation"></a><dl>
<dt><b>SNMP_ERRORSTATUS_NOCREATION</b></dt>
</dl>
</td>
<td width="60%">
The variable does not exist, and the agent cannot create it.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></a><a id="snmp_errorstatus_inconsistentvalue"></a><dl>
<dt><b>SNMP_ERRORSTATUS_INCONSISTENTVALUE</b></dt>
</dl>
</td>
<td width="60%">
The value is inconsistent with values of other managed objects.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></a><a id="snmp_errorstatus_resourceunavailable"></a><dl>
<dt><b>SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
Assigning the value to the variable requires allocation of resources that are currently unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_COMMITFAILED"></a><a id="snmp_errorstatus_commitfailed"></a><dl>
<dt><b>SNMP_ERRORSTATUS_COMMITFAILED</b></dt>
</dl>
</td>
<td width="60%">
No validation errors occurred, but no variables were updated.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_UNDOFAILED"></a><a id="snmp_errorstatus_undofailed"></a><dl>
<dt><b>SNMP_ERRORSTATUS_UNDOFAILED</b></dt>
</dl>
</td>
<td width="60%">
No validation errors occurred. Some variables were updated because it was not possible to undo their assignment.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></a><a id="snmp_errorstatus_authorizationerror"></a><dl>
<dt><b>SNMP_ERRORSTATUS_AUTHORIZATIONERROR</b></dt>
</dl>
</td>
<td width="60%">
An authorization error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_NOTWRITABLE"></a><a id="snmp_errorstatus_notwritable"></a><dl>
<dt><b>SNMP_ERRORSTATUS_NOTWRITABLE</b></dt>
</dl>
</td>
<td width="60%">
The variable exists but the agent cannot modify it.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></a><a id="snmp_errorstatus_inconsistentname"></a><dl>
<dt><b>SNMP_ERRORSTATUS_INCONSISTENTNAME</b></dt>
</dl>
</td>
<td width="60%">
The variable does not exist; the agent cannot create it because the named object instance is inconsistent with the values of other managed objects.

</td>
</tr>
</table>

### -param pErrorIndex [out]

Pointer to a variable to receive the error index result.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

The SNMP service calls the 
<b>SnmpExtensionQueryEx</b> function multiple times to process an incoming SNMP SET request. The service can call 
<b>SnmpExtensionQueryEx</b> during the 
TEST request phase, the 
COMMIT request phase, the 
UNDO request phase, and the 
CLEANUP request phase.

<h3><a id="_snmp_test_request"></a><a id="_SNMP_TEST_REQUEST"></a>TEST request</h3>
The SNMP service processes an SNMP SET request type by first calling the 
<b>SnmpExtensionQueryEx</b> function with a <i>dwRequestType</i> of SNMP_EXTENSION_SET_TEST. The service calls each extension agent responsible for the variable bindings in the request. Each extension agent must validate the variables in the variable binding list. They can optionally store any context information required for the following requests in the variable pointed to by the <i>pContextInfo</i> parameter.

If the TEST request fails, the service initiates a CLEANUP request. The service calls each extension agent that previously returned <b>TRUE</b> to the TEST request again with the 
<b>SnmpExtensionQueryEx</b> function. The service calls each extension agent using the SNMP_EXTENSION_SET_CLEANUP <i>dwRequestType</i>.

<h3><a id="_snmp_commit_request"></a><a id="_SNMP_COMMIT_REQUEST"></a>COMMIT request</h3>
If all extension agents return <b>TRUE</b> to the TEST request, the SNMP service calls each extension agent with the 
<b>SnmpExtensionQueryEx</b> function, using the SNMP_EXTENSION_SET_COMMIT <i>dwRequestType</i>. The service returns to the extension agent context information that the extension agent passed to the service. This is the context information the extension agent passed in the <i>pContextInfo</i> parameter during the TEST request. The extension agent can use the context information to update the values of the specified variables in an instrumentation-specific manner.

If the extension agent supports rollback processing, it can update the context information in the <i>pContextInfo</i> parameter at this time. The SNMP service passes the information back to the extension agent during the UNDO request.

If all extension agents return <b>TRUE</b> to the COMMIT request, the service calls each extension agent with the 
<b>SnmpExtensionQueryEx</b> function, using the SNMP_EXTENSION_SET_CLEANUP <i>dwRequestType</i>.

If any extension agent fails the COMMIT request, the service also initiates a CLEANUP request. The service calls each extension agent that previously returned <b>TRUE</b> to the COMMIT request again with the 
<b>SnmpExtensionQueryEx</b> function. The service calls each extension agent using the SNMP_EXTENSION_SET_CLEANUP <i>dwRequestType</i>.

<h3><a id="_snmp_cleanup_request"></a><a id="_SNMP_CLEANUP_REQUEST"></a>CLEANUP request</h3>
The service returns to the extension agent the context information passed in the <i>pContextInfo</i> parameter during the TEST or COMMIT request. The extension agent must release the resources associated with the parameter at this time.

<h3><a id="_snmp_undo_request"></a><a id="_SNMP_UNDO_REQUEST"></a>UNDO request</h3>
If any extension agent returns <b>FALSE</b> to the COMMIT request, the SNMP service terminates the COMMIT request. The service calls each extension agent that returned <b>TRUE</b> to the COMMIT request with a <i>dwRequestType</i> of SNMP_EXTENSION_SET_UNDO. This signals the extension agents that the COMMIT request failed, and they must initiate rollback processing.

The extension agents must attempt to reset the values of the variables of interest, back to the values they were before the COMMIT request failed. To do this, the extension agents use the context information returned in the <i>pContextInfo</i> parameter during the COMMIT request.

If any extension agent returns <b>FALSE</b> to the UNDO request, the entire SET operation fails with the error code SNMP_ERRORSTATUS_UNDOFAILED. If all extension agents return <b>TRUE</b> to the UNDO request, the SNMP SET operation fails with the error code set by the extension agent that failed the COMMIT request.

After the UNDO request the service always calls each extension agent with the 
<b>SnmpExtensionQueryEx</b> function, using the SNMP_EXTENSION_SET_CLEANUP <i>dwRequestType</i>.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionquery">SnmpExtensionQuery</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a>