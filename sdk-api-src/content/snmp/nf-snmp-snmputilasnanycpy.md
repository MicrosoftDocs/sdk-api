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

# SnmpUtilAsnAnyCpy function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilAsnAnyCpy</b> function copies the variable pointed to by the <i>pAnySrc</i> parameter to the <i>pAnyDst</i> parameter. The function allocates any necessary memory for the destination's copy. The 
<b>SnmpUtilAsnAnyCpy</b> function is an element of the SNMP Utility API.


## -parameters




### -param pAnyDst [out]

Pointer to an 
<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a> structure to receive the copy.


### -param pAnySrc [in]

Pointer to an 
<b>AsnAny</b> structure to copy.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/b18c3722-398e-4659-ab1c-edd09d5c220d">SnmpUtilAsnAnyFree</a> function to free the memory that the 
<b>SnmpUtilAsnAnyCpy</b> function allocates for the destination structure.




## -see-also




<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/b18c3722-398e-4659-ab1c-edd09d5c220d">SnmpUtilAsnAnyFree</a>
 

 

