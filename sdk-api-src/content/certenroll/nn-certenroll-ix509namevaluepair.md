---
UID: NN:certenroll.IX509NameValuePair
title: IX509NameValuePair
author: windows-driver-content
description: Represents a generic name-value pair.
old-location: security\ix509namevaluepair.htm
old-project: SecCertEnroll
ms.assetid: e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509NameValuePair, IX509NameValuePair interface [Security], IX509NameValuePair interface [Security],described, certenroll/IX509NameValuePair, security.ix509namevaluepair
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509NameValuePair
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509NameValuePair interface


## -description


The <b>IX509NameValuePair</b> interface represents a generic name-value pair. Although there are a few common name-value pairs created by the certificate request and enrollment process, you can use this object to specify any name and value. An <a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a> collection can be retrieved from an <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> object and an <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> object. The collections are not related.


<dl>
<dt><a id="name-value_pairs_and_the_enrollment_object_"></a><a id="NAME-VALUE_PAIRS_AND_THE_ENROLLMENT_OBJECT_"></a>name-value pairs and the enrollment object:</dt>
<dd>
Before an <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> object submits a certificate request to a certification authority (CA), the name-value collection is encoded as a concatenated  attribute string that has the format <i>Name1</i>:<i>Value1</i>\<i>Name2</i>:<i>Value2</i>\. You can retrieve the collection by calling the <a href="https://msdn.microsoft.com/d682fb7c-de80-4285-baa2-f86c997f0987">NameValuePairs</a> property. You can use the <a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a> object to add name-value pairs to the collection.

</dd>
</dl>
<dl>
<dt><a id="name-value_pairs_and_the_CMC_request_object_"></a><a id="name-value_pairs_and_the_cmc_request_object_"></a><a id="NAME-VALUE_PAIRS_AND_THE_CMC_REQUEST_OBJECT_"></a>name-value pairs and the CMC request object:</dt>
<dd>
A CMC request object (<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>) contains sequences of <b>TaggedAttribute</b>, <b>TaggedRequest</b>, and <b>TaggedContentInfo</b> ASN.1 structures. For more information,  see <a href="https://msdn.microsoft.com/faeee338-bce4-4b35-9be9-72a6568fa259">CMC Attributes</a>


The <b>TaggedAttribute</b> structure can contain a <b>RegInfo</b> attribute. This attribute consists of a byte array that contains the name-value pair collection. The byte array is created in the following manner:<ul>
<li>Each name-value string is standardized. For example, "%5C" escapes are substituted for backslash (\) characters.</li>
<li>Each name-value pair is concatenated by using an equal sign (=).</li>
<li>All of the pairs are concatenated by using an ampersand (&amp;)between each pair.</li>
<li>The result is encoded as a UTF-8 string.</li>
</ul>


The following example shows the ASN.1 output for a CMC certificate that contains a <b>RegInfo</b> attribute that contains a single name-value pair of "RequesterName=Domain\TargetUser".

<pre class="syntax" xml:space="preserve"><code>
...
30 33              ; SEQUENCE (33 Bytes)
   02 01                            ; INTEGER (1 Bytes)
   |  02
   06 08                            ; OBJECT_ID (8 Bytes)
   |  2b 06 01 05 05 07 07 12
   |     ; 1.3.6.1.5.5.7.7.18 Reg Info
   31 24                ; SET (24 Bytes)
      04 22 ; OCTET_STRING (22 Bytes)
      52 65 71 75 65 73 74 65  72 4e 61 6d 65 3d 44 6f  ; RequesterName=Do
      6d 61 69 6e 25 35 43 54  61 72 67 65 74 55 73 65  ; main%5CTargetUse
      72 26                                             ; r&amp; 
...
</code></pre>
</dd>
</dl>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509NameValuePair</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509NameValuePair</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509NameValuePair</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from strings that contain the  name and associated value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509NameValuePair</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="63%">
Retrieves the name portion of the name-value pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>


</td>
<td align="left" width="63%">
Retrieves the value portion of the name-value pair.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a>
 

 

