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

# _CRYPT_XML_TRANSFORM_INFO structure


## -description


The <b>CRYPT_XML_TRANSFORM_INFO</b> structure contains information that is used when applying the data transform.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field wszAlgorithm

A pointer to a null-terminated Unicode string that contains the <b>Algorithm</b> attribute.


### -field cbBufferSize

The size, in bytes, of the data provider's buffer. The size can be zero if the size cannot be determined at initialization time.
    This value is used by a caller of the structure pointed to by the <b>pfnCreateTransform</b> member to determine the necessary size of the receiving buffer.


### -field dwFlags

Specifies values that control how the transform is applied.


This member can be one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_TRANSFORM_ON_STREAM"></a><a id="crypt_xml_transform_on_stream"></a><dl>
<dt><b>CRYPT_XML_TRANSFORM_ON_STREAM</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Specifies that the input to the transform is a stream of bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_TRANSFORM_ON_NODESET"></a><a id="crypt_xml_transform_on_nodeset"></a><dl>
<dt><b>CRYPT_XML_TRANSFORM_ON_NODESET</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Specifies that the input to the transform is an XML node set.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_TRANSFORM_URI_QUERY_STRING"></a><a id="crypt_xml_transform_uri_query_string"></a><dl>
<dt><b>CRYPT_XML_TRANSFORM_URI_QUERY_STRING</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Specifies that the URI comparison is to be performed on the core URI 
without the QueryString.

In some cases, the URI may contain additional information 
in the QueryString after the ampersand (&amp;). Use this flag to evaluate only the core URI.

</td>
</tr>
</table>
 


### -field pfnCreateTransform

A pointer to a <a href="https://msdn.microsoft.com/d9228015-d5e7-4c72-9561-be4ee5fa4264">PFN_CRYPT_XML_CREATE_TRANSFORM</a> callback function used to create the transform.


## -remarks



For XML canonicalization transforms, the buffer size specified by the <b>cbBufferSize</b> member must be large enough to accommodate an entire <b>Start</b> element with all attribute values.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/012bad01-228a-4bb0-b883-0c2c7abd9271">Digital Signature Cryptographic Algorithms</a>
 

 

