---
UID: NF:winsnmp.SnmpCleanupEx
title: SnmpCleanupEx function
author: windows-sdk-content
description: The SnmpCleanupEx function performs cleanup when there are no outstanding successful calls to SnmpStartup or SnmpStartupEx within a Windows SNMP (WinSNMP) application.
old-location: snmp\snmpcleanupex.htm
tech.root: SNMP
ms.assetid: e6521c35-a58e-4b8e-b415-b49954187736
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SnmpCleanupEx, SnmpCleanupEx function [SNMP], _snmp_snmpcleanupex, snmp.snmpcleanupex, winsnmp/SnmpCleanupEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SnmpCleanupEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpCleanupEx function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
				<b>SnmpCleanupEx</b> function performs cleanup when there are no outstanding successful calls to <a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> or <a href="https://msdn.microsoft.com/5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a">SnmpStartupEx</a> within a Windows SNMP (WinSNMP) application. Otherwise, an internal reference count indicating the current number of outstanding successful calls to <b>SnmpStartupEx</b> is decremented.

This function should be used instead of <a href="https://msdn.microsoft.com/348f06e6-b408-4962-a0bc-8ff3e2ee21fa">SnmpCleanup</a> if Windows Server 2003 with Service Pack 1 (SP1) or later is installed. <b>SnmpCleanupEx</b> enables support for multiple independent software modules that use WinSNMP within the same application. 
<div class="alert"><b>Note</b>  A WinSNMP application must call the 
<b>SnmpCleanupEx</b> function for each successful call to <a href="https://msdn.microsoft.com/5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a">SnmpStartupEx</a>  before the application terminates.</div><div> </div>

## -parameters






## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS. Until the WinSNMP application successfully recalls the 
corresponding <a href="https://msdn.microsoft.com/5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a">SnmpStartupEx</a> function and there are no additional outstanding successful calls to either <a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> or <b>SnmpStartupEx</b>, any other call to a WinSNMP function within the same application returns SNMPAPI_FAILURE, with an extended error code of SNMPAPI_NOT_INITIALIZED.

If the function fails, the return value is SNMPAPI_FAILURE, but the WinSNMP application does not need to retry the call to 
<b>SnmpCleanupEx</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
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
<a href="https://msdn.microsoft.com/5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a">SnmpStartupEx</a> function did not complete successfully, or an unknown or undefined error occurred.

</td>
</tr>
</table>
 




## -remarks



Before the WinSNMP application calls 
<b>SnmpCleanupEx</b>, it should call the 
<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a> function once for each session the implementation opens as a result of a call to the 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a> function.

When a WinSNMP application calls the 
<b>SnmpCleanupEx</b> function, the implementation deallocates all resources allocated to the application if there are also no outstanding successful calls to  either <a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> or <a href="https://msdn.microsoft.com/5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a">SnmpStartupEx</a>. However, it is recommended that a WinSNMP application free the specific resources that the implementation allocates for it with the WinSNMP function that corresponds to the resource. For additional information about freeing individual resources, see 
<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a>, 
<a href="https://msdn.microsoft.com/d9175523-bbf0-4e20-b4da-140a6ee0ebd4">SnmpFreeVbl</a>, 
<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>, 
<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>, and 
<a href="https://msdn.microsoft.com/243e52aa-2b05-4c41-9f89-cf9c66517da6">SnmpFreePdu</a>.

If a WinSNMP application must perform an emergency exit, and it calls 
<b>SnmpCleanupEx</b> without freeing individual resources and without calling 
<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a> for every open session, the implementation deallocates all resources allocated to the WinSNMP application. However, to enable this functionality in the implementation, the application must still call 
<b>SnmpCleanupEx</b>.

<b>SnmpCleanupEx</b> must not be called when the application DLL is in the process of unloading.




## -see-also




<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a>



<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a>



<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>



<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>



<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a>



<a href="https://msdn.microsoft.com/243e52aa-2b05-4c41-9f89-cf9c66517da6">SnmpFreePdu</a>



<a href="https://msdn.microsoft.com/d9175523-bbf0-4e20-b4da-140a6ee0ebd4">SnmpFreeVbl</a>



<a href="https://msdn.microsoft.com/5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a">SnmpStartupEx</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

