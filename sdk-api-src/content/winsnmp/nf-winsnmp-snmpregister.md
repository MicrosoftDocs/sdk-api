---
UID: NF:winsnmp.SnmpRegister
title: SnmpRegister function
author: windows-sdk-content
description: The WinSNMP SnmpRegister function registers or unregisters a WinSNMP application for trap and notification reception. The application can register and receive traps and notifications, or unregister and disable traps and notifications.
old-location: snmp\snmpregister.htm
old-project: snmp
ms.assetid: ea2476b4-2f98-4295-95c4-c96c6b719e05
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SnmpRegister, SnmpRegister function [SNMP], _snmp_snmpregister, snmp.snmpregister, winsnmp/SnmpRegister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsnmp.h
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpRegister
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpRegister function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpRegister</b> function registers or unregisters a WinSNMP application for trap and notification reception. The application can register and receive traps and notifications, or unregister and disable traps and notifications.

A WinSNMP application can register or unregister for one type of trap or notification, or for all traps and notifications, depending on the value of the <i>notification</i> parameter.


## -parameters




### -param session [in]

Handle to the WinSNMP session that is registering or unregistering for traps and notifications.


### -param srcEntity [in]

Handle to the management entity that is the source of the registration request. This entity, acting in an SNMP manager role, will receive the trap or notification. 


Because the implementation does not use this parameter to filter traps and notifications from reaching the WinSNMP application,  a WinSNMP manager application typically passes <b>NULL</b> in this parameter.

If this parameter is <b>NULL</b>, the Microsoft WinSNMP implementation registers or unregisters all sources of trap and notification requests.

Note that the <i>srcEntity</i> parameter to the 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> function has a different role. In that function, <i>srcEntity</i> receives a handle to the entity that sent the trap.


### -param dstEntity [in]

Handle to the management entity that is the recipient of the registration request. This entity, acting in an SNMP agent role, will send the trap or notification. 




If this parameter is <b>NULL</b>, the implementation registers or unregisters the WinSNMP application for traps and notifications from all management entities.

Note that the <i>dstEntity</i> parameter to the 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> function receives a handle to the management entity that registers for trap notification.


### -param context [in]

Handle to the context, which is a set of managed object resources. 




If this parameter is <b>NULL</b>, the implementation registers or unregisters the WinSNMP application for traps and notifications for every context.


### -param notification [in]

Pointer to an 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure that contains the pattern-matching sequence for one type of trap or notification. The implementation uses this sequence to identify the type of trap or notification for which the WinSNMP application is registering or unregistering. For additional information, see the following Remarks section. 




If this parameter is <b>NULL</b>, the implementation registers or unregisters the WinSNMP application for all traps and notifications from the management entity or entities specified by the <i>dstEntity</i> parameter.


### -param state [in]

Specifies an unsigned long integer variable that indicates whether the WinSNMP application is registering to receive traps and notifications, or if it is unregistering. This parameter should be equal to one of the following values, but if it contains a different value, the implementation registers the application. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
Disable traps and notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_ON"></a><a id="snmpapi_on"></a><dl>
<dt><b>SNMPAPI_ON</b></dt>
</dl>
</td>
<td width="60%">
Register to receive traps and notifications.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a>. The 
<b>SnmpGetLastError</b> function may return one of the following WinSNMP or network transport layer errors.

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
<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> function did not complete successfully.

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
<dt><b>SNMPAPI_SESSION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>session</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
One or both of the entity parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_CONTEXT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>context</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>notification</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The network transport layer was not initialized, or the SNMPTRAP.EXE service could not be started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The trap port is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The network subsystem failed.

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
 

For additional information, see 
<a href="https://msdn.microsoft.com/2ff535b1-76cb-42aa-baeb-14c1a1bc41ce">Network Transport Errors</a>.




## -remarks



Typically a WinSNMP manager application, rather than an agent application, calls the 
<b>SnmpRegister</b> function.

It is important to note that for users who are not administrators, the 
<b>SnmpRegister</b> function succeeds on Windows 2000 and Windows XP only if the SNMP trap service has been started.

If a WinSNMP application passes <b>NULL</b> in a call to the 
<b>SnmpRegister</b> function in the <i>srcEntity</i>, <i>dstEntity</i>, <i>context</i>, or <i>notification</i> parameters, the implementation does not use that parameter to filter traps and notifications from reaching the WinSNMP application. If an application passes <b>NULL</b> in all of the parameters mentioned previously, the implementation delivers all received notifications to the session.

If a WinSNMP application registers to receive a specific type of trap or notification, it must define an object identifier, that is, an 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure, that corresponds to that type of trap. The <i>notification</i> parameter must point to this structure. RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers. For additional information, see 
<a href="https://msdn.microsoft.com/2bccba35-bf5c-4e5c-94e4-59980f2b9776">Managing Traps and Notifications</a> and 
<a href="https://msdn.microsoft.com/472f67ba-05d5-46f7-a2f1-1cef6182574e">Translating Traps from SNMPv1 to SNMPv2C</a>.

The implementation uses the value of the <i>notification</i> parameter as a pattern to match against received traps and notifications. For example, if the WinSNMP application passes n number of subidentifiers in the <i>notification</i> parameter, and the first n subidentifiers in a received trap match all the passed subidentifiers, then the trap object identifier is a match. If a received trap has fewer subidentifiers than n, the object identifier does not match. If there is a match, the implementation sends the trap or notification to the WinSNMP application.

If any or all of the <i>dstEntity</i>, <i>srcEntity</i>, or <i>context</i> parameters are <b>NULL</b>, the implementation may need to allocate resources on a subsequent call to the 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> function, for that function's corresponding parameters. When the WinSNMP application no longer needs the resources 
<b>SnmpRecvMsg</b> returns, the application must free the individual resources with the function that corresponds to the resource. For additional information, see 
<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a> and 
<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>.

For more information, see 
<a href="https://msdn.microsoft.com/76a4095f-ab5c-4f7a-9b60-a383a632fd65">Multiple Trap Registrations</a>.




## -see-also




<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a>



<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>



<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a>



<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

