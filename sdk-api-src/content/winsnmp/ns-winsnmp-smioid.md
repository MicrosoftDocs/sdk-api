---
UID: NS:winsnmp.__unnamed_struct_1
title: smiOID
author: windows-sdk-content
description: The WinSNMP smiOID structure passes object identifiers to multiple WinSNMP functions. The structure also receives the variable name of a variable binding entry in a call to the SnmpGetVb function.
old-location: snmp\smioid_str.htm
tech.root: SNMP
ms.assetid: 0bdf900e-6e67-4461-97bc-4c9650d888bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*smiLPOID, _snmp_smioid_str, smiLPOID, smiLPOID structure pointer [SNMP], smiOID, smiOID structure [SNMP], snmp.smioid_str, winsnmp/smiLPOID, winsnmp/smiOID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsnmp.h
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
 - Winsnmp.h
api_name:
 - smiOID
product: Windows
targetos: Windows
req.typenames: smiOID, *smiLPOID
req.redist: 
---

# smiOID structure


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>smiOID</b> structure passes object identifiers to multiple WinSNMP functions. The structure also receives the variable name of a variable binding entry in a call to the 
<a href="https://msdn.microsoft.com/a6598b4e-6797-4e18-8ab5-059c75bc84ef">SnmpGetVb</a> function.

The 
<b>smiOID</b> structure contains a pointer to a variable length array of a named object's subidentifiers. The structure can be a member of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa377997(v=VS.85).aspx">smiVALUE</a> structure.


## -struct-fields




### -field len

Specifies an unsigned long integer value that indicates the number of elements in the array pointed to by the <b>ptr</b> member.


### -field ptr

Pointer to an array of unsigned long integers that represent the object identifier's subidentifiers.


## -remarks



In an 
<b>smiOID</b> structure, the format of the array pointed to by the <b>ptr</b> member is one subidentifier per array element. For example, the string "1.3.6.1" would be an array of four elements {1,3,6,1}.

The Microsoft WinSNMP implementation allocates and deallocates memory for all output 
<b>smiOID</b> structures. The WinSNMP application should not free memory that the implementation allocates for the <b>ptr</b> member of an 
<b>smiOID</b> structure. Instead, the application must call the 
<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a> function to free the memory.

Because the WinSNMP application allocates memory for input descriptor objects with variable lengths, it must free that memory. For more information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.




## -see-also




<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>



<a href="https://msdn.microsoft.com/a6598b4e-6797-4e18-8ab5-059c75bc84ef">SnmpGetVb</a>



<a href="https://msdn.microsoft.com/aa13abb3-c16d-4b12-a3b8-9c3c727199e0">SnmpOidCompare</a>



<a href="https://msdn.microsoft.com/ab121160-1c4f-41c0-a738-2e7605780ed2">SnmpOidCopy</a>



<a href="https://msdn.microsoft.com/20f0af32-8f4f-4326-ab6a-389dc95be73f">SnmpOidToStr</a>



<a href="https://msdn.microsoft.com/cbcf8fc6-c5d6-476b-9490-4b87fd6a8a56">SnmpStrToOid</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/ec74217e-8d02-4bda-b365-7b8f6c14cffb">WinSNMP Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377997(v=VS.85).aspx">smiVALUE</a>
 

 

