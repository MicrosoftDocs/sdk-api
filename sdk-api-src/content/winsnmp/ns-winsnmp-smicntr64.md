---
UID: NS:winsnmp.smiCNTR64
title: smiCNTR64
author: windows-sdk-content
description: The WinSNMP smiCNTR64 structure contains a 64-bit unsigned integer value. The structure represents a 64-bit counter.
old-location: snmp\smicntr64_str.htm
old-project: snmp
ms.assetid: 224b162c-a9b3-4b71-a9ed-b15a51934498
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: "*smiLPCNTR64, _snmp_smicntr64_str, smiCNTR64, smiCNTR64 structure [SNMP], smiLPCNTR64, smiLPCNTR64 structure pointer [SNMP], snmp.smicntr64_str, winsnmp/smiCNTR64, winsnmp/smiLPCNTR64"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: smiCNTR64, *smiLPCNTR64
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsnmp.h
api_name:
 - smiCNTR64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# smiCNTR64 structure


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>smiCNTR64</b> structure contains a 64-bit unsigned integer value. The structure represents a 64-bit counter.


## -struct-fields




### -field hipart

Specifies the high-order 32 bits of the counter.


### -field lopart

Specifies the low-order 32 bits of the counter.


## -see-also




<a href="https://msdn.microsoft.com/a6598b4e-6797-4e18-8ab5-059c75bc84ef">SnmpGetVb</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/ec74217e-8d02-4bda-b365-7b8f6c14cffb">WinSNMP Structures</a>



<a href="https://msdn.microsoft.com/e5e8f321-54b2-469d-bdd3-9867fd85b447">smiVALUE</a>
 

 

