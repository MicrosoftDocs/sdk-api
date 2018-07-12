---
UID: NS:snmp.AsnOctetString
title: AsnOctetString
author: windows-sdk-content
description: The AsnOctetString structure contains octet quantities, usually bytes. This structure is used by multiple SNMP functions. This structure is not used by the WinSNMP API functions.
old-location: snmp\asnoctetstring_str.htm
old-project: snmp
ms.assetid: d58c54e2-0479-408f-977d-63409e5f500e
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: AsnBits, AsnDisplayString, AsnIPAddress, AsnImplicitSequence, AsnNetworkAddress, AsnOctetString, AsnOctetString structure [SNMP], AsnOpaque, AsnSequence, _snmp_asnoctetstring_str, snmp.asnoctetstring_str, snmp/AsnOctetString
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
req.typenames: AsnOctetString
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Snmp.h
api_name:
 - AsnOctetString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# AsnOctetString structure


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>AsnOctetString</b> structure contains octet quantities, usually bytes. This structure is used by multiple SNMP functions. This structure is not used by the 
<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API</a> functions.


## -struct-fields




### -field stream

Pointer to the octet stream.


### -field length

The number of octets in the data stream.


### -field dynamic

Flag that specifies whether the data stream has been dynamically allocated with the 
<a href="https://msdn.microsoft.com/85e293da-4c5b-4b32-9b86-e63074d37274">SnmpUtilMemAlloc</a> function.


## -remarks



Use the 
<b>AsnOctetString</b> structure to transfer string values. For example, use it to transfer the string that represents a computer name as a MIB object value.

You must check the flag specified in the <b>dynamic</b> member before you release the data stream of an octet string. Call the 
<a href="https://msdn.microsoft.com/57cf0398-d2c1-4dd9-ad77-0c453412034a">SnmpUtilMemFree</a> function only if the <b>dynamic</b> member is set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b6dacc85-893d-4825-93df-729333b491b3">SNMP Structures</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/85e293da-4c5b-4b32-9b86-e63074d37274">SnmpUtilMemAlloc</a>



<a href="https://msdn.microsoft.com/57cf0398-d2c1-4dd9-ad77-0c453412034a">SnmpUtilMemFree</a>
 

 

