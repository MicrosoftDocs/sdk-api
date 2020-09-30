---
UID: NF:snmp.SnmpSvcSetLogType
title: SnmpSvcSetLogType function (snmp.h)
description: The SnmpSvcSetLogType function adjusts the destination for the debug output from the SNMP service and from SNMP extension agents using the SnmpUtilDbgPrint function. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SNMP_OUTPUT_TO_CONSOLE","SNMP_OUTPUT_TO_DEBUGGER","SNMP_OUTPUT_TO_LOGFILE","SnmpSvcSetLogType","SnmpSvcSetLogType function [SNMP]","_snmp_snmpsvcsetlogtype","snmp.snmpsvcsetlogtype","snmp/SnmpSvcSetLogType"]
old-location: snmp\snmpsvcsetlogtype.htm
tech.root: SNMP
ms.assetid: 244a8359-9002-4ece-b340-20602d566a2c
ms.date: 12/05/2018
ms.keywords: SNMP_OUTPUT_TO_CONSOLE, SNMP_OUTPUT_TO_DEBUGGER, SNMP_OUTPUT_TO_LOGFILE, SnmpSvcSetLogType, SnmpSvcSetLogType function [SNMP], _snmp_snmpsvcsetlogtype, snmp.snmpsvcsetlogtype, snmp/SnmpSvcSetLogType
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
 - SnmpSvcSetLogType
 - snmp/SnmpSvcSetLogType
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
 - SnmpSvcSetLogType
---

# SnmpSvcSetLogType function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpSvcSetLogType</b> function adjusts the destination for the debug output from the SNMP service and from SNMP extension agents using the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputildbgprint">SnmpUtilDbgPrint</a> function. This function is an element of the SNMP Utility API.

## -parameters

### -param nLogType [in]

Specifies a signed integer variable that represents the destination for the debug output from the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputildbgprint">SnmpUtilDbgPrint</a> function. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_OUTPUT_TO_CONSOLE"></a><a id="snmp_output_to_console"></a><dl>
<dt><b>SNMP_OUTPUT_TO_CONSOLE</b></dt>
</dl>
</td>
<td width="60%">
The destination for the debug output is a console window.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_OUTPUT_TO_LOGFILE"></a><a id="snmp_output_to_logfile"></a><dl>
<dt><b>SNMP_OUTPUT_TO_LOGFILE</b></dt>
</dl>
</td>
<td width="60%">
The destination for the debug output is the SNMPDBG.LOG file in the SYSTEM32 directory.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_OUTPUT_TO_DEBUGGER"></a><a id="snmp_output_to_debugger"></a><dl>
<dt><b>SNMP_OUTPUT_TO_DEBUGGER</b></dt>
</dl>
</td>
<td width="60%">
The destination for the debug output is a debugger utility.

</td>
</tr>
</table>

## -returns

This function does not return a value.

## -remarks

Extension agents are encouraged to use the 
<b>SnmpSvcSetLogType</b> and 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetloglevel">SnmpSvcSetLogLevel</a> functions during development to adjust the output of debugging information. Extension agents can integrate the information with the debug output from the SNMP service.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcsetloglevel">SnmpSvcSetLogLevel</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputildbgprint">SnmpUtilDbgPrint</a>