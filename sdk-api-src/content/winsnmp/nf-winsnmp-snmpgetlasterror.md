---
UID: NF:winsnmp.SnmpGetLastError
title: SnmpGetLastError function (winsnmp.h)
description: The WinSNMP SnmpGetLastError function returns the calling application's last-error code value. The value indicates the reason why the last function call executed by the WinSNMP application failed.
helpviewer_keywords: ["SnmpGetLastError","SnmpGetLastError function [SNMP]","_snmp_snmpgetlasterror","snmp.snmpgetlasterror","winsnmp/SnmpGetLastError"]
old-location: snmp\snmpgetlasterror.htm
tech.root: SNMP
ms.assetid: 0cfb2bc3-cfa5-4806-9dcf-119541463e7b
ms.date: 12/05/2018
ms.keywords: SnmpGetLastError, SnmpGetLastError function [SNMP], _snmp_snmpgetlasterror, snmp.snmpgetlasterror, winsnmp/SnmpGetLastError
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
 - SnmpGetLastError
 - winsnmp/SnmpGetLastError
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
 - SnmpGetLastError
---

# SnmpGetLastError function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpGetLastError</b> function returns the calling application's last-error code value. The value indicates the reason why the last function call executed by the WinSNMP application failed.

## -parameters

### -param session [in]

Handle to the WinSNMP session. This parameter can also be <b>NULL</b>. 




In certain cases, when a function call fails you can pass a <b>NULL</b><i>session</i> value to the 
<b>SnmpGetLastError</b> function to retrieve the last-error code value. This is true for function calls that do not involve a <i>session</i> parameter, and cases in which the <i>session</i> parameter value is invalid. These cases are noted in the Return Values section on the function's reference page.

A single-thread application can pass a <b>NULL</b><i>session</i> value to 
<b>SnmpGetLastError</b> to retrieve last-error information for the entire application.

For more information, see the following Remarks and Return Values sections.

## -returns

If the <i>session</i> parameter is a valid WinSNMP session handle, the 
<b>SnmpGetLastError</b> function returns the last WinSNMP error that occurred for the indicated session.

If the <i>session</i> parameter is <b>NULL</b> — for example, if the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function fails, 
<b>SnmpGetLastError</b> returns the last WinSNMP error that occurred.

## -remarks

A WinSNMP application must call 
<b>SnmpGetLastError</b> immediately after a function fails, to retrieve the last-error code. If another function fails, it overwrites the last-error code set by the most recently failed function. For more information, see 
<a href="/windows/desktop/SNMP/winsnmp-error-codes">WinSNMP Error Codes</a>.

Although the <i>session</i> parameter accommodates both multithread and single-thread Windows operating environments, the potential still exists for the last-error code from one thread to overwrite the last-error code from another thread.

Note that 
<b>SnmpGetLastError</b> must be able to return the last-error code to a WinSNMP application under the following conditions:

<ul>
<li>After the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function fails</li>
<li>Before the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function creates any WinSNMP sessions for the instance of the application</li>
<li>After the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> function closes all WinSNMP sessions for the instance of the application</li>
<li>After the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> function disconnects the WinSNMP application from the Microsoft WinSNMP implementation</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>