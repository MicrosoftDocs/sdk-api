---
UID: NF:snmp.SnmpSvcSetLogLevel
title: SnmpSvcSetLogLevel function (snmp.h)
description: The SnmpSvcSetLogLevel function adjusts the level of detail of the debug output from the SNMP service and from SNMP extension agents using the SnmpUtilDbgPrint function. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SNMP_LOG_ERROR","SNMP_LOG_FATAL","SNMP_LOG_SILENT","SNMP_LOG_TRACE","SNMP_LOG_VERBOSE","SNMP_LOG_WARNING","SnmpSvcSetLogLevel","SnmpSvcSetLogLevel function [SNMP]","_snmp_snmpsvcsetloglevel","snmp.snmpsvcsetloglevel","snmp/SnmpSvcSetLogLevel"]
old-location: snmp\snmpsvcsetloglevel.htm
tech.root: SNMP
ms.assetid: 735eb056-1e2a-49d0-9613-10a326afb872
ms.date: 12/05/2018
ms.keywords: SNMP_LOG_ERROR, SNMP_LOG_FATAL, SNMP_LOG_SILENT, SNMP_LOG_TRACE, SNMP_LOG_VERBOSE, SNMP_LOG_WARNING, SnmpSvcSetLogLevel, SnmpSvcSetLogLevel function [SNMP], _snmp_snmpsvcsetloglevel, snmp.snmpsvcsetloglevel, snmp/SnmpSvcSetLogLevel
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
 - SnmpSvcSetLogLevel
 - snmp/SnmpSvcSetLogLevel
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
 - SnmpSvcSetLogLevel
---

# SnmpSvcSetLogLevel function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpSvcSetLogLevel</b> function adjusts the level of detail of the debug output from the SNMP service and from SNMP extension agents using the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputildbgprint">SnmpUtilDbgPrint</a> function. This function is an element of the SNMP Utility API.

## -parameters

### -param nLogLevel [in]

Specifies a signed integer variable that indicates the level of detail of the debug output from the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputildbgprint">SnmpUtilDbgPrint</a> function. This parameter can be one of the following values. 



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

## -returns

This function does not return a value.

## -remarks

Extension agents are encouraged to use the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetlogtype">SnmpSvcSetLogType</a> and 
<b>SnmpSvcSetLogLevel</b> functions during development to adjust the output of debugging information. Extension agents can integrate the information with the debug output from the SNMP service.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetlogtype">SnmpSvcSetLogType</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputildbgprint">SnmpUtilDbgPrint</a>