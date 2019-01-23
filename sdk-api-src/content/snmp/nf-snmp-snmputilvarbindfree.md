---
UID: NF:snmp.SnmpUtilVarBindFree
title: SnmpUtilVarBindFree function
author: windows-sdk-content
description: The SnmpUtilVarBindFree function frees the memory allocated for an SnmpVarBind structure. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilvarbindfree.htm
tech.root: SNMP
ms.assetid: 6e3d0a04-34f8-4342-837d-c0d357a1d1a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpUtilVarBindFree, SnmpUtilVarBindFree function [SNMP], _snmp_snmputilvarbindfree, snmp.snmputilvarbindfree, snmp/SnmpUtilVarBindFree
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
 - SnmpUtilVarBindFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilVarBindFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilVarBindFree</b> function frees the memory allocated for an 
<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a> structure. This function is an element of the SNMP Utility API.


## -parameters




### -param pVb [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a> structure whose memory should be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/79143aaa-26e1-4142-9c67-508d70034de2">SnmpUtilVarBindListFree</a>



<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a>
 

 

