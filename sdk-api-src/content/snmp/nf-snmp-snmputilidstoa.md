---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SnmpUtilIdsToA function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilIdsToA</b> function converts an object identifier (OID) to a null-terminated string. This function is an element of the SNMP Utility API.


## -parameters




### -param Ids [in]

Pointer to an array of unsigned integers. The array contains the sequence of numbers that the OID contains. The <i>IdLength</i> parameter specifies the array's length. 




For more information, see the following Return Values and Remarks sections.


### -param IdLength [in]

Specifies the number of elements in the array pointed to by the <i>Ids</i> parameter.


## -returns



The function returns a null-terminated string that contains the string representation of the array of numbers pointed to by the <i>Ids</i> parameter. The string contains a sequence of numbers separated by periods ('.'); for example, 1.3.6.1.4.1.311.

If the <i>Ids</i> parameter is null, or if the <i>IdLength</i> parameter specifies zero, the function returns the string "&lt;null oid&gt;".

The maximum length of the returned string is 256 characters. If the string's length exceeds 256 characters, the string is truncated and terminated with a sequence of three periods ('...').




## -remarks



The 
<b>SnmpUtilIdsToA</b> function can assist with the debugging of SNMP applications.

Note that the following memory restrictions apply when you call 
<b>SnmpUtilIdsToA</b>:

<ul>
<li>The <i>Ids</i> parameter must point to a valid memory block of at least <i>IdLength</i> integers, or the function call results in an access violation exception.</li>
<li>The string returned by 
<b>SnmpUtilIdsToA</b> resides in memory that the SNMP Utility API allocates. The application should not make any assumptions about the memory allocation. The data is guaranteed to be valid until you call 
<b>SnmpUtilIdsToA</b> again, so before calling the function again you should copy the data to another location.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/c21124ac-f2f8-4096-9100-639ded42d198">SnmpUtilOidToA</a>
 

 

