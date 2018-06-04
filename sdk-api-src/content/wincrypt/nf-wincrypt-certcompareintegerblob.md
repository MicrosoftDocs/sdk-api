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

# CertCompareIntegerBlob function


## -description


The <b>CertCompareIntegerBlob</b> function compares two integer <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOBs</a> to determine whether they represent equal numeric values. 


## -parameters




### -param pInt1 [in]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the first integer in the comparison.


### -param pInt2 [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the second integer in the comparison.


## -returns



If the representations of the integer BLOBs are identical and the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Before doing the comparison, most significant bytes with a value of 0x00 are removed from a positive number. Positive here means that the most significant bit in the next nonzero byte is not set.

Most significant bytes with a value of 0xFF are removed from a negative number. Negative here means that the most significant bit in the next non-0xFF byte is set. This produces the unique representation of that integer, as shown in the following table.

<table>
<tr>
<th>Original bytes</th>
<th>Reduced form</th>
</tr>
<tr>
<td>0xFFFFFF88</td>
<td>0xFF88</td>
</tr>
<tr>
<td>0xFF23</td>
<td>0xFF23</td>
</tr>
<tr>
<td>0x007F</td>
<td>0x7F</td>
</tr>
<tr>
<td>0x00000080</td>
<td>0x80</td>
</tr>
</table>
 

Multiple-byte integers are treated as <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a>. The least significant byte is <i>pbData</i>[0]. The most significant byte is <i>pbData</i>[<i>cbData</i> - 1], that is, 0xFFFFFF88 is stored in four bytes as:

{0x88, 0xFF, 0xFF, 0xFF}


#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/89186d98-80a9-460a-be2b-3e328675c485">Example C Program: Using CertOIDToAlgId and CertCompareIntegerBlob</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="cryptography_functions.htm">Data Management Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

