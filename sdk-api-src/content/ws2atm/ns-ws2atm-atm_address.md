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

# ATM_ADDRESS structure


## -description



			The 
<b>ATM_ADDRESS</b> structure holds ATM address data for ATM-based sockets.


## -struct-fields




### -field AddressType

Type of end-system ATM address.


### -field NumofDigits

Number of digits in the <b>Addr</b> parameter.


### -field Addr

Array representing the ATM address.


## -remarks



For ATM_E164, enter the numbered digits in the same order in which they would be entered on a numeric keypad; that is, the number digit that would be entered first is located in <b>addr</b>. Digits are coded in IA5 characters. Bit 8 is set to zero.

For ATM_NSAP, code the address using Binary Coded Decimal (BCD) as defined in the ATM Forum UNI 3.1. The <b>NumofDigits</b> field is ignored in this case, and the NSAP-style address always contains 20 bytes.

A value of SAP_FIELD_ANY in <b>AddressType</b> indicates that the <b>satm_number</b> field is a wildcard. There are two more specialized wildcard values: SAP_FIELD_ANY_AESA_SEL and SAP_FIELD_ANY_AESA_REST. SAP_FIELD_ANY_AESA_SEL means that this is an NSAP-style ATM Endsystem Address and the selector octet is set as a wildcard. SAP_FIELD_ANY_AESA_REST means that this is an NSAP-style ATM Endsystem Address and all the octets except for the selector octet are set as wildcards.




## -see-also




<a href="https://msdn.microsoft.com/6cbeb19f-0aa8-48a1-a46a-691edc542d5a">sockaddr_atm</a>
 

 

