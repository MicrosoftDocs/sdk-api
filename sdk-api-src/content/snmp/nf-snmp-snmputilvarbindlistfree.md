---
UID: NF:snmp.SnmpUtilVarBindListFree
title: SnmpUtilVarBindListFree function
author: windows-sdk-content
description: The SnmpUtilVarBindListFree function frees the memory allocated for an SnmpVarBindList structure. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilvarbindlistfree.htm
old-project: snmp
ms.assetid: 79143aaa-26e1-4142-9c67-508d70034de2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SnmpUtilVarBindListFree, SnmpUtilVarBindListFree function [SNMP], _snmp_snmputilvarbindlistfree, snmp.snmputilvarbindlistfree, snmp/SnmpUtilVarBindListFree
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
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilVarBindListFree
product: Windows
targetos: Windows
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpUtilVarBindListFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
				<b>SnmpUtilVarBindListFree</b> function frees the memory allocated for an 
<a href="https://msdn.microsoft.com/73e33a64-39fb-4e36-8267-88c78ec27e26">SnmpVarBindList</a> structure. This function is an element of the SNMP Utility API.


## -parameters




### -param pVbl [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/73e33a64-39fb-4e36-8267-88c78ec27e26">SnmpVarBindList</a> structure whose allocated memory should be freed.


## -returns



This function has no return values.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/6e3d0a04-34f8-4342-837d-c0d357a1d1a3">SnmpUtilVarBindFree</a>



<a href="https://msdn.microsoft.com/73e33a64-39fb-4e36-8267-88c78ec27e26">SnmpVarBindList</a>
 

 

