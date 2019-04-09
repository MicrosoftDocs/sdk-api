---
UID: NS:snmp.__unnamed_struct_4
title: SnmpVarBindList (snmp.h)
author: windows-sdk-content
description: The SnmpVarBindList structure represents an SNMP variable bindings list. This structure is used by multiple SNMP functions. This structure is not used by the WinSNMP API functions.
old-location: snmp\snmpvarbindlist_str.htm
tech.root: SNMP
ms.assetid: 73e33a64-39fb-4e36-8267-88c78ec27e26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpVarBindList, SnmpVarBindList structure [SNMP], _snmp_snmpvarbindlist_str, snmp.snmpvarbindlist_str, snmp/SnmpVarBindList
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Snmp.h
api_name:
 - SnmpVarBindList
product: Windows
targetos: Windows
req.typenames: SnmpVarBindList
req.redist: 
---

# SnmpVarBindList structure


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpVarBindList</b> structure represents an SNMP variable bindings list. This structure is used by multiple SNMP functions. This structure is not used by the 
<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API</a> functions.


## -struct-fields




### -field list

A pointer that references an array to access individual variable bindings.


### -field len

Contains the number of variable bindings in the list.


## -see-also




<a href="https://msdn.microsoft.com/b6dacc85-893d-4825-93df-729333b491b3">SNMP Structures</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a>
 

 

