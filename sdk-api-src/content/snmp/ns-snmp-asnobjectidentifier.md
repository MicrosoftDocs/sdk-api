---
UID: NS:snmp.AsnObjectIdentifier
title: AsnObjectIdentifier
author: windows-sdk-content
description: The AsnObjectIdentifier structure represents object identifiers. This structure is used by multiple SNMP functions. This structure is not used by the WinSNMP API functions.
old-location: snmp\asnobjectidentifier_str.htm
old-project: SNMP
ms.assetid: 695e5581-00df-49af-8abe-1dd1b25cb215
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: AsnObjectIdentifier, AsnObjectIdentifier structure [SNMP], AsnObjectName, _snmp_asnobjectidentifier_str, snmp.asnobjectidentifier_str, snmp/AsnObjectIdentifier
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AsnObjectIdentifier
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Snmp.h
api_name:
 - AsnObjectIdentifier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# AsnObjectIdentifier structure


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>AsnObjectIdentifier</b> structure represents object identifiers. This structure is used by multiple SNMP functions. This structure is not used by the 
<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API</a> functions.


## -struct-fields




### -field idLength

Specifies the number of integers in the object identifier.


### -field ids

Pointer to an array of integers that represents the object identifier.


## -see-also




<a href="https://msdn.microsoft.com/b6dacc85-893d-4825-93df-729333b491b3">SNMP Structures</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>
 

 

