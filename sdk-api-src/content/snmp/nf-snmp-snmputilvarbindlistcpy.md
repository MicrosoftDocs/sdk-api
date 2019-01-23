---
UID: NF:snmp.SnmpUtilVarBindListCpy
title: SnmpUtilVarBindListCpy function
author: windows-sdk-content
description: The SnmpUtilVarBindListCpy function copies the specified SnmpVarBindList structure, and allocates any necessary memory for the destination's copy. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilvarbindlistcpy.htm
tech.root: SNMP
ms.assetid: 19837eac-c5b0-46a6-b10d-4460cf918cba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpUtilVarBindListCpy, SnmpUtilVarBindListCpy function [SNMP], _snmp_snmputilvarbindlistcpy, snmp.snmputilvarbindlistcpy, snmp/SnmpUtilVarBindListCpy
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
 - SnmpUtilVarBindListCpy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilVarBindListCpy function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
				<b>SnmpUtilVarBindListCpy</b> function copies the specified 
<a href="https://msdn.microsoft.com/73e33a64-39fb-4e36-8267-88c78ec27e26">SnmpVarBindList</a> structure, and allocates any necessary memory for the destination's copy. This function is an element of the SNMP Utility API.


## -parameters




### -param pVblDst [out]

Pointer to an 
<a href="https://msdn.microsoft.com/73e33a64-39fb-4e36-8267-88c78ec27e26">SnmpVarBindList</a> structure to receive the copy.


### -param pVblSrc [in]

Pointer to an 
<a href="https://msdn.microsoft.com/73e33a64-39fb-4e36-8267-88c78ec27e26">SnmpVarBindList</a> structure to copy.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/79143aaa-26e1-4142-9c67-508d70034de2">SnmpUtilVarBindListFree</a> function to free memory that the 
<b>SnmpUtilVarBindListCpy</b> function allocates for the destination structure.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/65947bdb-1165-4e5d-b3ca-1c54cd50166e">SnmpUtilOidCpy</a>



<a href="https://msdn.microsoft.com/79143aaa-26e1-4142-9c67-508d70034de2">SnmpUtilVarBindListFree</a>



<a href="https://msdn.microsoft.com/73e33a64-39fb-4e36-8267-88c78ec27e26">SnmpVarBindList</a>
 

 

