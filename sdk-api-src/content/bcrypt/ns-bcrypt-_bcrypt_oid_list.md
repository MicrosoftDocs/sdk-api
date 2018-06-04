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

# _BCRYPT_OID_LIST structure


## -description


The <b>BCRYPT_OID_LIST</b> structure is used to contain a collection of <a href="https://msdn.microsoft.com/00143883-88f7-4b15-bdba-128ee255abf6">BCRYPT_OID</a> structures. Use this structure with the <a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">BCRYPT_HASH_OID_LIST</a> property to retrieve the list of hashing <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) that have been encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoding.


## -struct-fields




### -field dwOIDCount

The number of elements in the <b>pOIDs</b> array.


### -field pOIDs

The address of an array of <a href="https://msdn.microsoft.com/00143883-88f7-4b15-bdba-128ee255abf6">BCRYPT_OID</a> structures that contains OIDs.


## -remarks



The first OID in the <b>pOIDs</b> array is used to identify any hashes or signatures created by this algorithm provider. When verifying a hash or signature, all the OIDs in the array are treated as valid.

In the Microsoft Primitive Provider implementation, <b>dwOIDCount</b> is 2, so that the <b>pOIDs</b> array contains two members:

<ul>
<li><b>pOIDs[0]</b> contains a DER-encoded <b>AlgorithmIdentifier</b> with a <b>NULL</b> parameter.</li>
<li><b>pOIDs[1]</b> contains the DER-encoded <b>AlgorithmIdentifier</b> without a <b>NULL</b> parameter.</li>
</ul>
For example, the SHA-1 encoding would be:

<ul>
<li><b>pOIDs[0]</b> --&gt; 06 05 2b 0e 03 02 1a 05 00

</li>
<li><b>pOIDs[1]</b> --&gt; 06 05 2b 0e 03 02 1a</li>
</ul>


The following snippet describes an <b>AlgorithmIdentifier</b> in <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) notation.  <b>SEQUENCE</b>, <b>OBJECT IDENTIFIER</b>, and <b>ANY</b> are DER encoded. The <b>ANY</b> BLOB is <b>NULL</b>.

<pre class="syntax" xml:space="preserve"><code>AlgorithmIdentifier ::= SEQUENCE {
   algorithm            OBJECT IDENTIFIER,
   algorithmParams      ANY
}
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/00143883-88f7-4b15-bdba-128ee255abf6">BCRYPT_OID</a>



<a href="https://msdn.microsoft.com/5c62ca3a-843e-41a7-9340-41785fbb15f4">BCryptGetProperty</a>



<a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">Cryptography Primitive Property Identifiers</a>
 

 

