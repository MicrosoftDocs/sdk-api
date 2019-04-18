---
UID: NF:snmp.SnmpUtilVarBindCpy
title: SnmpUtilVarBindCpy function (snmp.h)
author: windows-sdk-content
description: The SnmpUtilVarBindCpy function copies the specified SnmpVarBind structure, and allocates any memory necessary for the destination structure. The SnmpUtilVarBindCpy function is an element of the SNMP Utility API.
old-location: snmp\snmputilvarbindcpy.htm
tech.root: SNMP
ms.assetid: 0a3e1fb8-360d-4bfa-8fa3-8c114b9fd681
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpUtilVarBindCpy, SnmpUtilVarBindCpy function [SNMP], _snmp_snmputilvarbindcpy, snmp.snmputilvarbindcpy, snmp/SnmpUtilVarBindCpy
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
 - SnmpUtilVarBindCpy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpUtilVarBindCpy function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilVarBindCpy</b> function copies the specified 
<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a> structure, and allocates any memory necessary for the destination structure. The 
<b>SnmpUtilVarBindCpy</b> function is an element of the SNMP Utility API.


## -parameters




### -param pVbDst [out]

Pointer to an 
<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a> structure to receive the copy.


### -param pVbSrc [in]

Pointer to an 
<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a> structure to copy.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/6e3d0a04-34f8-4342-837d-c0d357a1d1a3">SnmpUtilVarBindFree</a> function to free memory that the 
<b>SnmpUtilVarBindCpy</b> function allocates for the destination structure.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/6e3d0a04-34f8-4342-837d-c0d357a1d1a3">SnmpUtilVarBindFree</a>



<a href="https://msdn.microsoft.com/40f9930d-93d1-45eb-aa3a-499947004fcf">SnmpVarBind</a>
 

 

