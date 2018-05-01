---
UID: NF:winsnmp.SnmpStrToEntity
title: SnmpStrToEntity function
author: windows-driver-content
description: The WinSNMP SnmpStrToEntity function returns a handle to information about an SNMP management entity that is specific to the Microsoft WinSNMP implementation.
old-location: snmp\snmpstrtoentity.htm
old-project: SNMP
ms.assetid: d0a8e389-ba5b-45f4-9682-1fbe456daaed
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpStrToEntity, SnmpStrToEntity function [SNMP], _snmp_snmpstrtoentity, snmp.snmpstrtoentity, winsnmp/SnmpStrToEntity
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsnmp32.dll
api_name:
-	SnmpStrToEntity
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpStrToEntity function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpStrToEntity</b> function returns a handle to information about an SNMP management entity that is specific to the Microsoft WinSNMP implementation.


## -parameters




### -param session [in]

Handle to the WinSNMP session.


### -param string [in]

Pointer to a null-terminated string that identifies the SNMP management entity of interest. The current setting of the entity and context translation mode determines the manner in which 
<b>SnmpStrToEntity</b> interprets the input string as follows. 



<table>
<tr>
<th>Entity/Context Translation Mode</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_TRANSLATED"></a><a id="snmpapi_translated"></a><dl>
<dt><b>SNMPAPI_TRANSLATED</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a user-friendly name. The implementation translates the name into its SNMPv1 or SNMPv2C components using the implementation's database.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V1"></a><a id="snmpapi_untranslated_v1"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V1</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP transport address.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V2"></a><a id="snmpapi_untranslated_v2"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V2</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP transport address.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is a handle to the SNMP management entity of interest.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a>. The 
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
<dt><b>SNMPAPI_ENTITY_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The entity string is invalid.

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



The current setting of the entity and context translation mode determines the manner in which 
<b>SnmpStrToEntity</b> interprets the input string that identifies the management entity of interest. For additional information, see 
<a href="https://msdn.microsoft.com/b90b8e95-dab0-483b-9336-07e20c122cba">Support for IPX Address Strings in WinSNMP</a> and 
<a href="https://msdn.microsoft.com/2550f235-1351-440a-8b4e-f0d30b058229">Setting the Entity and Context Translation Mode</a>.

The WinSNMP application should call the 
<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a> function to release the entity handle allocated by the 
<b>SnmpStrToEntity</b> function. For additional information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.

The 
<b>SnmpStrToEntity</b> function returns a valid entity handle that a WinSNMP application can use as the <i>srcEntity</i> or the <i>dstEntity</i> parameter in multiple WinSNMP functions. These functions include the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>, 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a>, 
<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a>, 
<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a>, and 
<a href="https://msdn.microsoft.com/d19d6451-1640-4c3b-9e60-d9cb591cf173">SnmpDecodeMsg</a> functions.

The implementation returns the current entity and context translation mode in the <i>nTranslateMode</i> parameter of the 
<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> function. A WinSNMP application can change the setting of the entity and context translation mode with a call to the 
<a href="https://msdn.microsoft.com/8ee7e660-e718-40e6-adcd-1554eb7391d9">SnmpSetTranslateMode</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d19d6451-1640-4c3b-9e60-d9cb591cf173">SnmpDecodeMsg</a>



<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a>



<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a>



<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a>



<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/8ee7e660-e718-40e6-adcd-1554eb7391d9">SnmpSetTranslateMode</a>



<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

