---
UID: NF:mgmtapi.SnmpMgrTrapListen
title: SnmpMgrTrapListen function
author: windows-sdk-content
description: The SnmpMgrTrapListen function registers the ability of an SNMP manager application to receive SNMP traps from the SNMP Trap Service. This function is an element of the SNMP Management API.
old-location: snmp\snmpmgrtraplisten.htm
old-project: snmp
ms.assetid: 9ba799a7-0088-4939-9665-ce96074c6448
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SnmpMgrTrapListen, SnmpMgrTrapListen function [SNMP], _snmp_snmpmgrtraplisten, mgmtapi/SnmpMgrTrapListen, snmp.snmpmgrtraplisten
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mgmtapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SOURCE_GROUP_ENTRY, *PSOURCE_GROUP_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mgmtapi.dll
api_name:
 - SnmpMgrTrapListen
product: Windows
targetos: Windows
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SnmpMgrTrapListen function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrTrapListen</b> function registers the ability of an SNMP manager application to receive SNMP traps from the SNMP Trap Service. This function is an element of the SNMP Management API.


## -parameters




### -param phTrapAvailable [out]

Pointer to an event handle to receive an indication that there are traps available, and that the application should call the 
<a href="https://msdn.microsoft.com/ce773bbe-0a05-45b5-af80-fc594a83b87a">SnmpMgrGetTrap</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which may return any of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MEM_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Indicates a memory allocation error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_TRAP_DUPINIT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this function has already been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_TRAP_ERRORS</b></dt>
</dl>
</td>
<td width="60%">
Indicates one or more errors occurred; traps are not accessible. The application can attempt to call the function again.

</td>
</tr>
</table>
 

This function may return other system errors as well.




## -remarks



It is important to note that for users who are not administrators, the 
<b>SnmpMgrTrapListen</b> function succeeds only if the SNMP trap service has been started.

The application must always call the 
<b>SnmpMgrTrapListen</b> function before calling the 
<a href="https://msdn.microsoft.com/ce773bbe-0a05-45b5-af80-fc594a83b87a">SnmpMgrGetTrap</a> function. This is because the event handle pointed to by the <i>phTrapAvailable</i> parameter enables the event-driven acquisition of SNMP traps. The SNMP Management API signals an application's event when the SNMP Trap Service delivers a trap.

The application can also poll the 
<a href="https://msdn.microsoft.com/ce773bbe-0a05-45b5-af80-fc594a83b87a">SnmpMgrGetTrap</a> function for traps at regular intervals. In this case, the application should repeatedly call 
<b>SnmpMgrGetTrap</b> until the function returns zero.

<b>Windows Server 2003:  </b>SNMP manager applications can call 
<a href="https://msdn.microsoft.com/d8e7cc61-e313-4e36-88e7-686b4f9282b5">SnmpMgrClose</a> with a <b>NULL</b><i>session</i> parameter to clean up resources associated with a successful call to the 
<b>SnmpMgrTrapListen</b> function. Note, however, that if your application is a DLL, it should not call 
<b>SnmpMgrClose</b> from its 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> entry-point function.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/ce773bbe-0a05-45b5-af80-fc594a83b87a">SnmpMgrGetTrap</a>
 

 

