---
UID: NF:snmp.SnmpExtensionClose
title: SnmpExtensionClose function
author: windows-sdk-content
description: The Microsoft SNMP service calls the SnmpExtensionClose function to request that the SNMP extension agent deallocate resources and terminate operations. This function is an element of the SNMP Extension Agent API.
old-location: snmp\snmpextensionclose.htm
old-project: SNMP
ms.assetid: 19fcac27-daa1-40e2-9038-7f03279381f0
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SnmpExtensionClose, SnmpExtensionClose callback, SnmpExtensionClose callback function [SNMP], _snmp_snmpextensionclose, snmp.snmpextensionclose, snmp/SnmpExtensionClose
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
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Snmp.h
api_name:
-	SnmpExtensionClose
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpExtensionClose function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionClose</b> function to request that the SNMP extension agent deallocate resources and terminate operations. This function is an element of the SNMP Extension Agent API.


## -parameters






## -returns



This callback function does not return a value.




## -remarks



It is not necessary for the extension agent to call its own 
<b>SnmpExtensionClose</b> entry point. This is because the SNMP service calls the extension agent's 
<b>SnmpExtensionClose</b> function when the service unloads the extension agent from the service's address space. The extension agent can clean up allocated resources and terminate services at this time.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/015f2be2-8e10-4abd-afd0-f76834856733">SnmpExtensionInit</a>



<a href="https://msdn.microsoft.com/f4e090ca-3f15-4f50-8ea7-92a06868268f">SnmpExtensionInitEx</a>
 

 

