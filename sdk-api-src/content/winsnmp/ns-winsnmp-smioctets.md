---
UID: NS:winsnmp.smiOCTETS
title: smiOCTETS
author: windows-sdk-content
description: The WinSNMP smiOCTETS structure passes context strings to multiple WinSNMP functions. The structure also describes and receives encoded SNMP messages.
old-location: snmp\smioctets_str.htm
old-project: SNMP
ms.assetid: d53da0e8-ce7d-4923-90c3-2469cbd9d9b1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*smiLPBITS, *smiLPIPADDR, *smiLPNSAPADDR, *smiLPOCTETS, *smiLPOPAQUE, _snmp_smioctets_str, smiBITS, smiIPADDR, smiLPOCTETS, smiLPOCTETS structure pointer [SNMP], smiNSAPADDR, smiOCTETS, smiOCTETS structure [SNMP], smiOPAQUE, snmp.smioctets_str, winsnmp/smiLPOCTETS, winsnmp/smiOCTETS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsnmp.h
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
req.typenames: smiOCTETS, *smiLPOCTETS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsnmp.h
api_name:
 - smiOCTETS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# smiOCTETS structure


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>smiOCTETS</b> structure passes context strings to multiple WinSNMP functions. The structure also describes and receives encoded SNMP messages.

The 
<b>smiOCTETS</b> structure contains a pointer to an SNMP octet string of variable length. The structure can be a member of the 
<a href="https://msdn.microsoft.com/e5e8f321-54b2-469d-bdd3-9867fd85b447">smiVALUE</a> structure.


## -struct-fields




### -field len

Specifies an unsigned long integer value that indicates the number of bytes in the octet string array pointed to by the <b>ptr</b> member.


### -field ptr

Pointer to a byte array that contains the octet string of interest. A <b>NULL</b>-terminating byte is not required.


## -remarks



The Microsoft WinSNMP implementation allocates and deallocates memory for all output 
<b>smiOCTETS</b> structures. The WinSNMP application should not free memory that the implementation allocates for the <b>ptr</b> member of an 
<b>smiOCTETS</b> structure. Instead, the application must call the 
<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a> function to free the memory.

Because the WinSNMP application allocates memory for input descriptor objects with variable lengths, it must free that memory. For more information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.




## -see-also




<a href="https://msdn.microsoft.com/d82c352d-8685-4276-b58c-ce89557f074a">SnmpContextToStr</a>



<a href="https://msdn.microsoft.com/d19d6451-1640-4c3b-9e60-d9cb591cf173">SnmpDecodeMsg</a>



<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a>



<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>



<a href="https://msdn.microsoft.com/d552f453-cc19-4166-aca3-bbaa3669b1c8">SnmpStrToContext</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/ec74217e-8d02-4bda-b365-7b8f6c14cffb">WinSNMP Structures</a>



<a href="https://msdn.microsoft.com/e5e8f321-54b2-469d-bdd3-9867fd85b447">smiVALUE</a>
 

 

