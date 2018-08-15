---
UID: NF:snmp.SnmpExtensionInitEx
title: SnmpExtensionInitEx function
author: windows-sdk-content
description: The Microsoft SNMP service calls the SnmpExtensionInitEx function to identify any additional management information base (MIB) subtrees the SNMP extension agent supports. This function is an element of the SNMP Extension Agent API.
old-location: snmp\snmpextensioninitex.htm
old-project: snmp
ms.assetid: f4e090ca-3f15-4f50-8ea7-92a06868268f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SnmpExtensionInitEx, SnmpExtensionInitEx callback, SnmpExtensionInitEx callback function [SNMP], _snmp_snmpextensioninitex, snmp.snmpextensioninitex, snmp/SnmpExtensionInitEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: snmp.h
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
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Snmp.h
api_name:
 - SnmpExtensionInitEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpExtensionInitEx function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionInitEx</b> function to identify any additional management information base (MIB) subtrees the SNMP extension agent supports. This function is an element of the SNMP Extension Agent API.


## -parameters




### -param pNextSupportedRegion [out]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to receive the next MIB subtree that the extension agent supports.


## -returns



If the <i>pNextSupportedRegion</i> parameter has been initialized with an additional MIB subtree, the return value is <b>TRUE</b>.

If there are no more MIB subtrees to register, the return value is <b>FALSE</b>.




## -remarks



The SNMP service repeatedly calls the 
<b>SnmpExtensionInitEx</b> function entry point so the extension agent can register support for additional MIB subtrees.

The SNMP service makes a copy of the 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure the extension agent returns in the <i>pNextSupportedRegion</i> parameter. The extension agent must allocate and deallocate the resources associated with the original structure. It can do this when the SNMP service calls the 
<a href="https://msdn.microsoft.com/19fcac27-daa1-40e2-9038-7f03279381f0">SnmpExtensionClose</a> function.




## -see-also




<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/19fcac27-daa1-40e2-9038-7f03279381f0">SnmpExtensionClose</a>



<a href="https://msdn.microsoft.com/015f2be2-8e10-4abd-afd0-f76834856733">SnmpExtensionInit</a>



<a href="https://msdn.microsoft.com/40468bf2-0e91-448b-a2e5-b84b786c67a2">SnmpExtensionMonitor</a>
 

 

