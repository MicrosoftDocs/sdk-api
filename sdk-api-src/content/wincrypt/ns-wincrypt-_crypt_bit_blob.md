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

# _CRYPT_BIT_BLOB structure


## -description


The <b>CRYPT_BIT_BLOB</b> structure contains a set of bits represented by an array of bytes.


## -struct-fields




### -field cbData

The number of bytes in the <b>pbData</b> array.


### -field pbData

A pointer to an array of bytes that represents the bits.


### -field cUnusedBits

The number of unused bits in the last byte of the array. The unused bits are always the least significant bits in the last byte of the array.


## -remarks



Because the smallest chunk of memory that can normally be allocated is a byte, the <b>CRYPT_BIT_BLOB</b> structure allows the last byte in the array to contain zero to seven unused bits. The number of unused bits in the array is contained  in the <b>cUnusedBits</b> member of this structure. The number of meaningful bits in the <b>pbData</b> member is calculated with the formula ((<b>cbData</b> × 8) –
				<b>cUnusedBits</b>). For example, if you need to represent 10 bits, you would allocate an array of 2 bytes and set <b>cUnusedBits</b> to 6. If you view the array as contiguous bits from left to right, the left 10 bits would be meaningful, and the right 6 bits would be unused.




## -see-also




<a href="https://msdn.microsoft.com/6603b627-5e5d-48bc-b200-c8dcdd646994">CERT_BASIC_CONSTRAINTS_INFO</a>



<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/cedf0321-4f5a-48a9-abfd-d8642bb89576">CERT_KEY_ATTRIBUTES_INFO</a>



<a href="https://msdn.microsoft.com/f949c8e5-055d-4919-abcc-441880ccce56">CERT_KEY_USAGE_RESTRICTION_INFO</a>



<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a>



<a href="https://msdn.microsoft.com/f650765e-7a72-42a3-baf7-29779fd04adc">CERT_SIGNED_CONTENT_INFO</a>
 

 

