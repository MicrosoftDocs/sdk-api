---
UID: NF:snmp.SnmpSvcGetUptime
title: SnmpSvcGetUptime function
author: windows-sdk-content
description: The SnmpSvcGetUptime function retrieves the number of centiseconds that the SNMP service has been running. This function is an element of the SNMP Utility API.
old-location: snmp\snmpsvcgetuptime.htm
tech.root: SNMP
ms.assetid: 46702e39-3ea2-471c-9281-3cd7dcae9c9c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpSvcGetUptime, SnmpSvcGetUptime function [SNMP], _snmp_snmpsvcgetuptime, snmp.snmpsvcgetuptime, snmp/SnmpSvcGetUptime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpSvcGetUptime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpSvcGetUptime function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpSvcGetUptime</b> function retrieves the number of centiseconds that the SNMP service has been running. This function is an element of the SNMP Utility API.


## -parameters






## -returns



The function returns a <b>DWORD</b> value that is the number of centiseconds the SNMP service has been running.




## -remarks



An extension agent should call the 
<b>SnmpSvcGetUptime</b> function only if the extension agent DLL is loaded within the address space of the SNMP service.

The SNMP extension agent DLL is encouraged to use the 
<b>SnmpSvcGetUptime</b> function to retrieve the number of centiseconds that the SNMP service has been running. Extension agents should use 
<b>SnmpSvcGetUptime</b> rather than calculate the uptime using the <i>dwUptimeReference</i> parameter. The service passes this parameter to the extension agent as the result of a call to the 
<a href="https://msdn.microsoft.com/015f2be2-8e10-4abd-afd0-f76834856733">SnmpExtensionInit</a> function. Because the <i>dwUptimeReference</i> parameter stores the elapsed time as a <b>DWORD</b> value in milliseconds, the time can wrap to zero and reflect an inaccurate time interval.

An extension agent that sends traps must initialize the <i>timeStamp</i> parameter to the 
<a href="https://msdn.microsoft.com/5c768bf5-aa25-4ead-8ee9-fc1f30de4354">SnmpExtensionTrap</a> function with the value returned by a call to the 
<b>SnmpSvcGetUptime</b> function.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/015f2be2-8e10-4abd-afd0-f76834856733">SnmpExtensionInit</a>



<a href="https://msdn.microsoft.com/5c768bf5-aa25-4ead-8ee9-fc1f30de4354">SnmpExtensionTrap</a>
 

 

