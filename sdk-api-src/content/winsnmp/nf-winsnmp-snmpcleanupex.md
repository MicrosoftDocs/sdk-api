---
UID: NF:winsnmp.SnmpCleanupEx
title: SnmpCleanupEx function (winsnmp.h)
description: The SnmpCleanupEx function performs cleanup when there are no outstanding successful calls to SnmpStartup or SnmpStartupEx within a Windows SNMP (WinSNMP) application.
helpviewer_keywords: ["SnmpCleanupEx","SnmpCleanupEx function [SNMP]","_snmp_snmpcleanupex","snmp.snmpcleanupex","winsnmp/SnmpCleanupEx"]
old-location: snmp\snmpcleanupex.htm
tech.root: SNMP
ms.assetid: e6521c35-a58e-4b8e-b415-b49954187736
ms.date: 12/05/2018
ms.keywords: SnmpCleanupEx, SnmpCleanupEx function [SNMP], _snmp_snmpcleanupex, snmp.snmpcleanupex, winsnmp/SnmpCleanupEx
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
 - SnmpCleanupEx
 - winsnmp/SnmpCleanupEx
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
 - SnmpCleanupEx
---

# SnmpCleanupEx function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
				<b>SnmpCleanupEx</b> function performs cleanup when there are no outstanding successful calls to <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> or <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartupex">SnmpStartupEx</a> within a Windows SNMP (WinSNMP) application. Otherwise, an internal reference count indicating the current number of outstanding successful calls to <b>SnmpStartupEx</b> is decremented.

This function should be used instead of <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> if Windows Server 2003 with Service Pack 1 (SP1) or later is installed. <b>SnmpCleanupEx</b> enables support for multiple independent software modules that use WinSNMP within the same application. 
<div class="alert"><b>Note</b>  A WinSNMP application must call the 
<b>SnmpCleanupEx</b> function for each successful call to <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartupex">SnmpStartupEx</a>  before the application terminates.</div><div> </div>



## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS. Until the WinSNMP application successfully recalls the 
corresponding <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartupex">SnmpStartupEx</a> function and there are no additional outstanding successful calls to either <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> or <b>SnmpStartupEx</b>, any other call to a WinSNMP function within the same application returns SNMPAPI_FAILURE, with an extended error code of SNMPAPI_NOT_INITIALIZED.

If the function fails, the return value is SNMPAPI_FAILURE, but the WinSNMP application does not need to retry the call to 
<b>SnmpCleanupEx</b>. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
<b>SnmpGetLastError</b> function can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartupex">SnmpStartupEx</a> function did not complete successfully, or an unknown or undefined error occurred.

</td>
</tr>
</table>

## -remarks

Before the WinSNMP application calls 
<b>SnmpCleanupEx</b>, it should call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> function once for each session the implementation opens as a result of a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function.

When a WinSNMP application calls the 
<b>SnmpCleanupEx</b> function, the implementation deallocates all resources allocated to the application if there are also no outstanding successful calls to  either <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> or <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartupex">SnmpStartupEx</a>. However, it is recommended that a WinSNMP application free the specific resources that the implementation allocates for it with the WinSNMP function that corresponds to the resource. For additional information about freeing individual resources, see 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>, and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>.

If a WinSNMP application must perform an emergency exit, and it calls 
<b>SnmpCleanupEx</b> without freeing individual resources and without calling 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> for every open session, the implementation deallocates all resources allocated to the WinSNMP application. However, to enable this functionality in the implementation, the application must still call 
<b>SnmpCleanupEx</b>.

<b>SnmpCleanupEx</b> must not be called when the application DLL is in the process of unloading.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartupex">SnmpStartupEx</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>
