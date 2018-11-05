---
UID: NF:cryptxml.CryptXmlOpenToDecode
title: CryptXmlOpenToDecode function
author: windows-sdk-content
description: Opens an XML digital signature to decode and returns the handle of the document context that encapsulates a CRYPT_XML_SIGNATURE structure. The document context can include one or more Signature elements.
old-location: security\cryptxmlopentodecode.htm
tech.root: seccrypto
ms.assetid: b6a77d62-b92d-4b83-949f-14a0ce3ce025
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CRYPT_XML_FLAG_DISABLE_EXTENSIONS, CRYPT_XML_FLAG_NO_SERIALIZE, CryptXmlOpenToDecode, CryptXmlOpenToDecode function [Security], cryptxml/CryptXmlOpenToDecode, security.cryptxmlopentodecode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlOpenToDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlOpenToDecode function


## -description


The <b>CryptXmlOpenToDecode</b> function opens an XML digital signature to decode 
 and returns the handle of the document context that encapsulates a <a href="https://msdn.microsoft.com/en-us/library/Dd433864(v=VS.85).aspx">CRYPT_XML_SIGNATURE</a> structure. 
 The document context can include one or more <b>Signature</b> elements.


## -parameters




### -param pConfig [in, optional]

The handle of the transform chain engine. 
    If this parameter is <b>NULL</b>, then a default engine will be 
    used to apply transforms.


### -param dwFlags

A <b>DWORD</b> value that controls which CryptXML extensions are loaded and whether the XML is serialized. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_NO_SERIALIZE"></a><a id="crypt_xml_flag_no_serialize"></a><dl>
<dt><b>CRYPT_XML_FLAG_NO_SERIALIZE</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Inhibit serialization.


<div class="alert"><b>Important</b>  Do not set this flag when multiple threads are accessing a CryptXml object. Serialization ensures mutual exclusion when two or more threads attempt 
to simultaneously accept a CryptXml object or memory.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_DISABLE_EXTENSIONS"></a><a id="crypt_xml_flag_disable_extensions"></a><dl>
<dt><b>CRYPT_XML_FLAG_DISABLE_EXTENSIONS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Only default implementations for the signature and digest are used. When this flag is set, no other registered extensions are loaded.

</td>
</tr>
</table>
 


### -param rgProperty [in]

A pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Dd433860(v=VS.85).aspx">CRYPT_XML_PROPERTY</a> structures that contain additional properties.


### -param cProperty

The number of items in the array pointed to by the <i>rgProperty</i> parameter.


### -param pEncoded [in]

A pointer to <a href="https://msdn.microsoft.com/en-us/library/Dd433844(v=VS.85).aspx">CRYPT_XML_BLOB</a> structure that contains the signature to decode.


### -param phCryptXml

The handle of a Document Context object.  When you have finished using the handle, release it by passing it to the <a href="https://msdn.microsoft.com/en-us/library/Dd433806(v=VS.85).aspx">CryptXmlClose</a> function.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



