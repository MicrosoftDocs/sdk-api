---
UID: NF:snmp.SnmpUtilDbgPrint
title: SnmpUtilDbgPrint function (snmp.h)
description: The SnmpUtilDbgPrint function enables debugging output from the SNMP service. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SNMP_LOG_ERROR","SNMP_LOG_FATAL","SNMP_LOG_SILENT","SNMP_LOG_TRACE","SNMP_LOG_VERBOSE","SNMP_LOG_WARNING","SnmpUtilDbgPrint","SnmpUtilDbgPrint function [SNMP]","_snmp_snmputildbgprint","snmp.snmputildbgprint","snmp/SnmpUtilDbgPrint"]
old-location: snmp\snmputildbgprint.htm
tech.root: SNMP
ms.assetid: ab092155-192f-450f-9635-9c34a4f572aa
ms.date: 12/05/2018
ms.keywords: SNMP_LOG_ERROR, SNMP_LOG_FATAL, SNMP_LOG_SILENT, SNMP_LOG_TRACE, SNMP_LOG_VERBOSE, SNMP_LOG_WARNING, SnmpUtilDbgPrint, SnmpUtilDbgPrint function [SNMP], _snmp_snmputildbgprint, snmp.snmputildbgprint, snmp/SnmpUtilDbgPrint
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
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpUtilDbgPrint
 - snmp/SnmpUtilDbgPrint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilDbgPrint
---

# SnmpUtilDbgPrint function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilDbgPrint</b> function enables debugging output from the SNMP service. This function is an element of the SNMP Utility API.

## -parameters

### -param nLogLevel [in]

Specifies a signed integer variable that indicates the level of detail of the log event. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_SILENT"></a><a id="snmp_log_silent"></a><dl>
<dt><b>SNMP_LOG_SILENT</b></dt>
</dl>
</td>
<td width="60%">
Disable all debugging output.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_FATAL"></a><a id="snmp_log_fatal"></a><dl>
<dt><b>SNMP_LOG_FATAL</b></dt>
</dl>
</td>
<td width="60%">
Display fatal errors only.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_ERROR"></a><a id="snmp_log_error"></a><dl>
<dt><b>SNMP_LOG_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Display recoverable errors.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_WARNING"></a><a id="snmp_log_warning"></a><dl>
<dt><b>SNMP_LOG_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Display warnings and recoverable errors.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_TRACE"></a><a id="snmp_log_trace"></a><dl>
<dt><b>SNMP_LOG_TRACE</b></dt>
</dl>
</td>
<td width="60%">
Display trace information.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_VERBOSE"></a><a id="snmp_log_verbose"></a><dl>
<dt><b>SNMP_LOG_VERBOSE</b></dt>
</dl>
</td>
<td width="60%">
Display verbose trace information.

</td>
</tr>
</table>

### -param szFormat [in]

Pointer to a null-terminated format string that is similar to the standard C library function <b>printf</b> style.

### -param ...

Additional parameters.

## -returns

This function does not return a value.

## -remarks

Extension agents are encouraged to use this function during development to enable debug output from the SNMP service.

Use the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetloglevel">SnmpSvcSetLogLevel</a> function to set the level of detail of the debug output from the SNMP service or from an extension agent's call to the 
<b>SnmpUtilDbgPrint</b> function. Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetlogtype">SnmpSvcSetLogType</a> function to specify the destination for the debug output.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetloglevel">SnmpSvcSetLogLevel</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetlogtype">SnmpSvcSetLogType</a>