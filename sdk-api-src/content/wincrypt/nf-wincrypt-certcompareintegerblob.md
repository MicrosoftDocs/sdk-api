---
UID: NF:wincrypt.CertCompareIntegerBlob
title: CertCompareIntegerBlob function
author: windows-sdk-content
description: The CertCompareIntegerBlob function compares two integer BLOBs to determine whether they represent equal numeric values.
old-location: security\certcompareintegerblob.htm
old-project: SecCrypto
ms.assetid: 467ce464-2f22-4583-a745-711ba3b05f4f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CertCompareIntegerBlob, CertCompareIntegerBlob function [Security], _crypto2_certcompareintegerblob, security.certcompareintegerblob, wincrypt/CertCompareIntegerBlob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertCompareIntegerBlob
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
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



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

