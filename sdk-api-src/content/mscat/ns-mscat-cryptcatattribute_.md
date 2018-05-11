---
UID: NS:mscat.CRYPTCATATTRIBUTE_
title: CRYPTCATATTRIBUTE_
author: windows-driver-content
description: The CRYPTCATATTRIBUTE structure defines a catalog attribute. This structure is used by the CryptCATEnumerateAttr and CryptCATEnumerateCatAttr functions.
old-location: security\cryptcatattribute.htm
old-project: SecCrypto
ms.assetid: 41b91303-f3eb-4288-9ad2-98f170680988
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CRYPTCATATTRIBUTE, CRYPTCATATTRIBUTE structure [Security], CRYPTCATATTRIBUTE_, CRYPTCAT_ATTR_AUTHENTICATED, CRYPTCAT_ATTR_DATAASCII, CRYPTCAT_ATTR_DATABASE64, CRYPTCAT_ATTR_DATAREPLACE, CRYPTCAT_ATTR_NAMEASCII, CRYPTCAT_ATTR_NAMEOBJID, CRYPTCAT_ATTR_UNAUTHENTICATED, mscat/CRYPTCATATTRIBUTE, security.cryptcatattribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRYPTCATATTRIBUTE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mscat.h
api_name:
-	CRYPTCATATTRIBUTE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# CRYPTCATATTRIBUTE_ structure


## -description


<p class="CCE_Message">[The  <b>CRYPTCATATTRIBUTE</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTCATATTRIBUTE</b> structure defines a catalog attribute. This structure is used by the <a href="https://msdn.microsoft.com/064e87db-4330-4b8b-9865-ba8b9714f6e4">CryptCATEnumerateAttr</a> and <a href="https://msdn.microsoft.com/57b6ff5c-e47e-41ac-8ec8-01a47ea77acf">CryptCATEnumerateCatAttr</a> functions.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field pwszReferenceTag

A pointer to a null-terminated string that contains the reference tag value.


### -field dwAttrTypeAndAction

Bitwise combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_AUTHENTICATED"></a><a id="cryptcat_attr_authenticated"></a><dl>
<dt><b>CRYPTCAT_ATTR_AUTHENTICATED</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
The attribute is authenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_UNAUTHENTICATED"></a><a id="cryptcat_attr_unauthenticated"></a><dl>
<dt><b>CRYPTCAT_ATTR_UNAUTHENTICATED</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The attribute is unauthenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_NAMEASCII"></a><a id="cryptcat_attr_nameascii"></a><dl>
<dt><b>CRYPTCAT_ATTR_NAMEASCII</b></dt>
<dt>             0x00000001</dt>
</dl>
</td>
<td width="60%">
The attribute is an ASCII string.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_NAMEOBJID"></a><a id="cryptcat_attr_nameobjid"></a><dl>
<dt><b>CRYPTCAT_ATTR_NAMEOBJID</b></dt>
<dt>             0x00000002</dt>
</dl>
</td>
<td width="60%">
The attribute is a cryptographic object identifier (OID).

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_DATAASCII"></a><a id="cryptcat_attr_dataascii"></a><dl>
<dt><b>CRYPTCAT_ATTR_DATAASCII</b></dt>
<dt>             0x00010000</dt>
</dl>
</td>
<td width="60%">
The attribute contains simple ASCII characters that should not be decoded.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_DATABASE64"></a><a id="cryptcat_attr_database64"></a><dl>
<dt><b>CRYPTCAT_ATTR_DATABASE64</b></dt>
<dt>            0x00020000</dt>
</dl>
</td>
<td width="60%">
The attribute is in base 64 format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_DATAREPLACE"></a><a id="cryptcat_attr_datareplace"></a><dl>
<dt><b>CRYPTCAT_ATTR_DATAREPLACE</b></dt>
<dt>           0x00040000</dt>
</dl>
</td>
<td width="60%">
The attribute replaces the value for an existing attribute.

</td>
</tr>
</table>
 


### -field cbValue

Number of bytes used by <b>pbValue</b>.


### -field pbValue

A pointer to the encoded bytes.


### -field dwReserved

Reserved; do not use.


## -see-also




<a href="https://msdn.microsoft.com/064e87db-4330-4b8b-9865-ba8b9714f6e4">CryptCATEnumerateAttr</a>



<a href="https://msdn.microsoft.com/57b6ff5c-e47e-41ac-8ec8-01a47ea77acf">CryptCATEnumerateCatAttr</a>
 

 

