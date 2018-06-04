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

# CryptXmlCreateReference function


## -description


The <b>CryptXmlCreateReference</b> function creates a reference to an XML signature.


## -parameters




### -param hCryptXml [in]

The handle of the XML signature.


### -param dwFlags

Specifies flags that affect how the reference is created.


Currently defined <i>dwFlags</i> values are shown in the following table.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_CREATE_REFERENCE_AS_OBJECT"></a><a id="crypt_xml_flag_create_reference_as_object"></a><dl>
<dt><b>CRYPT_XML_FLAG_CREATE_REFERENCE_AS_OBJECT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set this flag to create an <b>Object</b> node and add it to the <b>Signature</b> element. A reference to the <b>Object</b>  node is created in the <b>SignedInfo</b> element.

The returned handle is an encapsulated <b>Object</b> node and can be used in subsequent calls to the <b>CryptXmlCreateReference</b> function to create references in the <b>Manifest</b> node.

</td>
</tr>
</table>
 


### -param wszId [in, optional]

 A pointer to a <b>null</b>-terminated Unicode string that contains the value of the ID attribute of the <b>Reference</b> element of the signature.
	If this parameter is <b>NULL</b>, then the <b>ID</b> attribute is not created.
	If this parameter is an empty string, then the <b>ID</b> attribute with empty
        value is created.


### -param wszURI [in, optional]

A pointer to a <b>null</b>-terminated Unicode string that contains the value of the URI attribute of the <b>Reference</b> element of the signature.
    If this parameter is an empty string,
    then the URI attribute with an empty value is created.


### -param wszType [in, optional]

A pointer to a <b>null</b>-terminated Unicode string that contains the value of the Type attribute of the <b>Reference</b> element of the signature.
    The processing engine does not check or use this attribute.


### -param pDigestMethod [in]

A pointer to a <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that contains the digest method.


### -param cTransform

The number of elements in the array pointed to by the <i>rgTransform</i> parameter.


### -param rgTransform [in]

A pointer to an ordered array of <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structures that contain transform algorithms to be applied to
    the reference data before the digest calculation.



### -param phReference [out]

A pointer to a reference handle.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



