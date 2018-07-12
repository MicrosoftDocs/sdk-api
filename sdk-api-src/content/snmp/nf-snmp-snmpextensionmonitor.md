---
UID: NF:snmp.SnmpExtensionMonitor
title: SnmpExtensionMonitor function
author: windows-sdk-content
description: The Microsoft SNMP service calls the SnmpExtensionMonitor function to provide the SNMP extension agent with a view to the service's internal counters and parameters. This function is an element of the SNMP Extension Agent API.
old-location: snmp\snmpextensionmonitor.htm
old-project: snmp
ms.assetid: 40468bf2-0e91-448b-a2e5-b84b786c67a2
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: SnmpExtensionMonitor, SnmpExtensionMonitor callback, SnmpExtensionMonitor callback function [SNMP], _snmp_snmpextensionmonitor, snmp.snmpextensionmonitor, snmp/SnmpExtensionMonitor
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
 - SnmpExtensionMonitor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpExtensionMonitor function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionMonitor</b> function to provide the SNMP extension agent with a view to the service's internal counters and parameters. This function is an element of the SNMP Extension Agent API.

The 
<b>SnmpExtensionMonitor</b> function is optional. Extension agents should implement the function if they are interested in a view of the SNMP service's internal management objects, as defined in RFC 1213, "Management Information Base for Network Management of TCP/IP-based internets: MIB-II."


## -parameters




### -param pAgentMgmtData [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a> objects (structures). The number of objects, and the type and description of each object, are in accordance with RFC 1213. For more information, see the following Remarks section.


## -returns



Unless an unexpected error occurs while the SNMP extension agent is processing the value of the <i>pAgentMgmtData</i> parameter, the extension agent should return <b>TRUE</b>. If the extension agent returns <b>FALSE</b>, the SNMP service does not load the extension agent, and the service stops directing SNMP requests to the extension agent.




## -remarks



If the extension agent exports the 
<b>SnmpExtensionMonitor</b> function, the SNMP service calls the function during initialization of the extension agent, immediately after the service calls the 
<a href="https://msdn.microsoft.com/015f2be2-8e10-4abd-afd0-f76834856733">SnmpExtensionInit</a> and the 
<a href="https://msdn.microsoft.com/f4e090ca-3f15-4f50-8ea7-92a06868268f">SnmpExtensionInitEx</a> functions.

The SNMP service dynamically updates the SNMP counters (for example, the snmpInPkts and the snmpOutNoSuchNames counters) in the array pointed to by the <i>pAgentMgmtData</i> parameter. In order to be able to read these values while the SNMP service is running, the extension agent must store the pointer to <i>pAgentMgmtData</i>.

Note that an SNMP extension agent should not update the memory pointed to by the <i>pAgentMgmtData</i> parameter. This is because the values of the SNMP service's internal counters would no longer be valid, and the behavior of the SNMP service could become unpredictable. As long as the extension agent does not alter it, the memory pointed to by <i>pAgentMgmtData</i> is valid while the SNMP service is running.




## -see-also




<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/19fcac27-daa1-40e2-9038-7f03279381f0">SnmpExtensionClose</a>



<a href="https://msdn.microsoft.com/015f2be2-8e10-4abd-afd0-f76834856733">SnmpExtensionInit</a>



<a href="https://msdn.microsoft.com/f4e090ca-3f15-4f50-8ea7-92a06868268f">SnmpExtensionInitEx</a>
 

 

