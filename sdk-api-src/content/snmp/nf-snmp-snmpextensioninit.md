---
UID: NF:snmp.SnmpExtensionInit
title: SnmpExtensionInit function
author: windows-sdk-content
description: The Microsoft SNMP service calls the SnmpExtensionInit function to initialize the SNMP extension agent DLL. This function is an element of the SNMP Extension Agent API.
old-location: snmp\snmpextensioninit.htm
old-project: snmp
ms.assetid: 015f2be2-8e10-4abd-afd0-f76834856733
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: SnmpExtensionInit, SnmpExtensionInit callback, SnmpExtensionInit callback function [SNMP], _snmp_snmpextensioninit, snmp.snmpextensioninit, snmp/SnmpExtensionInit
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Snmp.h
api_name:
 - SnmpExtensionInit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpExtensionInit function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionInit</b> function to initialize the SNMP extension agent DLL. This function is an element of the SNMP Extension Agent API.


## -parameters




### -param dwUptimeReference [in]

Specifies a time-zero reference for the extension agent. 




<div class="alert"><b>Note</b>  Extension agents should ignore this parameter. The SNMP extension agent DLL should use the 
<a href="https://msdn.microsoft.com/46702e39-3ea2-471c-9281-3cd7dcae9c9c">SnmpSvcGetUptime</a> function to retrieve the number of centiseconds the SNMP service has been running. For more information, see the following Remarks section.</div>
<div> </div>

### -param phSubagentTrapEvent [out]

Pointer to an event handle the extension agent passes back to the SNMP service. This handle is used to notify the service that the extension agent has one or more traps to send. For additional information about allocating and deallocating the event handle, see the following Remarks section.


### -param pFirstSupportedRegion [out]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to receive the first MIB subtree that the extension agent supports. For additional information about allocating and deallocating resources for this structure, see the following Remarks section. 




The extension agent can register additional MIB subtrees by implementing the 
<a href="https://msdn.microsoft.com/f4e090ca-3f15-4f50-8ea7-92a06868268f">SnmpExtensionInitEx</a> entry point function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



Extension agents should ignore the <i>dwUptimeReference</i> parameter. Instead, they should call the 
<a href="https://msdn.microsoft.com/46702e39-3ea2-471c-9281-3cd7dcae9c9c">SnmpSvcGetUptime</a> function to retrieve the number of centiseconds that the Microsoft SNMP service has been running. Because the <i>dwUptimeReference</i> parameter stores the elapsed time as a <b>DWORD</b> value in milliseconds, the time can wrap to zero and reflect an inaccurate time interval.

The extension agent notifies the SNMP service that it needs to send one or more traps by setting the event handle passed back in the <i>phSubagentTrapEvent</i> parameter to the signaled state. After this event has been signaled, the SNMP service repeatedly calls the extension agent's 
<a href="https://msdn.microsoft.com/5c768bf5-aa25-4ead-8ee9-fc1f30de4354">SnmpExtensionTrap</a> entry point until the function returns a value of <b>FALSE</b>. This indicates that the extension agent has no more traps to send. If the extension agent does not generate traps, the <i>phSubagentTrapEvent</i> parameter should return a value of <b>NULL</b>.

The SNMP extension agent must allocate and deallocate resources for the trap event handle. When the SNMP service calls the 
<b>SnmpExtensionInit</b> function, the extension agent must call the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function to allocate the event handle. The extension agent passes the handle to the SNMP service in the <i>phSubagentTrapEvent</i> parameter. When the SNMP service calls the 
<a href="https://msdn.microsoft.com/19fcac27-daa1-40e2-9038-7f03279381f0">SnmpExtensionClose</a> function, the extension agent must deallocate resources for the trap event handle.

The SNMP service makes a copy of the 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure the extension agent returns in the <i>pFirstSupportedRegion</i> parameter. The extension agent must allocate and deallocate the resources associated with the original structure. It can do this when the SNMP service calls the 
<a href="https://msdn.microsoft.com/19fcac27-daa1-40e2-9038-7f03279381f0">SnmpExtensionClose</a> function.




## -see-also




<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a>



<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/19fcac27-daa1-40e2-9038-7f03279381f0">SnmpExtensionClose</a>



<a href="https://msdn.microsoft.com/40468bf2-0e91-448b-a2e5-b84b786c67a2">SnmpExtensionMonitor</a>



<a href="https://msdn.microsoft.com/5c768bf5-aa25-4ead-8ee9-fc1f30de4354">SnmpExtensionTrap</a>



<a href="https://msdn.microsoft.com/46702e39-3ea2-471c-9281-3cd7dcae9c9c">SnmpSvcGetUptime</a>
 

 

