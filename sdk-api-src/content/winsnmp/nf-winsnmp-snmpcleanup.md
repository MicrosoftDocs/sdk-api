---
UID: NF:winsnmp.SnmpCleanup
title: SnmpCleanup function (winsnmp.h)
description: The SnmpCleanup function informs the Microsoft WinSNMP implementation that the calling WinSNMP application no longer requires the implementation's services.
old-location: snmp\snmpcleanup.htm
tech.root: SNMP
ms.assetid: 348f06e6-b408-4962-a0bc-8ff3e2ee21fa
ms.date: 12/05/2018
ms.keywords: SnmpCleanup, SnmpCleanup function [SNMP], _snmp_snmpcleanup, snmp.snmpcleanup, winsnmp/SnmpCleanup
ms.topic: function
f1_keywords:
- winsnmp/SnmpCleanup
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wsnmp32.dll
api_name:
- SnmpCleanup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpCleanup function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
				<b>SnmpCleanup</b> function informs the Microsoft WinSNMP implementation that the calling WinSNMP application no longer requires the implementation's services.
<div class="alert"><b>Note</b>  A WinSNMP application must call the 
<b>SnmpCleanup</b> function as the last WinSNMP function before it terminates.</div><div> </div>

## -parameters






## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS. Until the WinSNMP application successfully recalls the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function, any other call to a WinSNMP function returns SNMPAPI_FAILURE, with an extended error code of SNMPAPI_NOT_INITIALIZED.

If the function fails, the return value is SNMPAPI_FAILURE, but the WinSNMP application does not need to retry the call to 
<b>SnmpCleanup</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its<i> session</i> parameter. The 
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
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

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
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>
 




## -remarks



Before the WinSNMP application calls 
<b>SnmpCleanup</b>, it should call the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> function once for each session the implementation opens as a result of a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function.

When a WinSNMP application calls the 
<b>SnmpCleanup</b> function, the implementation deallocates all resources allocated to the application. However, it is recommended that a WinSNMP application free the specific resources that the implementation allocates for it with the WinSNMP function that corresponds to the resource. For additional information about freeing individual resources, see 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>.

If a WinSNMP application must perform an emergency exit, and it calls 
<b>SnmpCleanup</b> without freeing individual resources and without calling 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> for every open session, the implementation deallocates all resources allocated to the WinSNMP application. However, to enable this functionality in the implementation, the application must still call 
<b>SnmpCleanup</b>.

<b>SnmpCleanup</b> must not be called when the application DLL is in the process of unloading.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>
 

 

