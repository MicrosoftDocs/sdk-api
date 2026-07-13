---
UID: NN:certenroll.IX509NameValuePair
title: IX509NameValuePair (certenroll.h)
description: Represents a generic name-value pair.
helpviewer_keywords: ["IX509NameValuePair","IX509NameValuePair interface [Security]","IX509NameValuePair interface [Security]","described","certenroll/IX509NameValuePair","security.ix509namevaluepair"]
old-location: security\ix509namevaluepair.htm
tech.root: security
ms.assetid: e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3
ms.date: 12/05/2018
ms.keywords: IX509NameValuePair, IX509NameValuePair interface [Security], IX509NameValuePair interface [Security],described, certenroll/IX509NameValuePair, security.ix509namevaluepair
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509NameValuePair
 - certenroll/IX509NameValuePair
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509NameValuePair
---

# IX509NameValuePair interface


## -description

The <b>IX509NameValuePair</b> interface represents a generic name-value pair. Although there are a few common name-value pairs created by the certificate request and enrollment process, you can use this object to specify any name and value. An <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a> collection can be retrieved from an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object and an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> object. The collections are not related.


<dl>
<dt><a id="name-value_pairs_and_the_enrollment_object_"></a><a id="NAME-VALUE_PAIRS_AND_THE_ENROLLMENT_OBJECT_"></a> name-value pairs and the enrollment object:</dt>
<dd>
Before an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object submits a certificate request to a certification authority (CA), the name-value collection is encoded as a concatenated  attribute string that has the format <i>Name1</i>:<i>Value1</i>&#92;<i>Name2</i>:<i>Value2</i>\. You can retrieve the collection by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_namevaluepairs">NameValuePairs</a> property. You can use the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a> object to add name-value pairs to the collection.

</dd>
</dl>
<dl>
<dt><a id="name-value_pairs_and_the_CMC_request_object_"></a><a id="name-value_pairs_and_the_cmc_request_object_"></a><a id="NAME-VALUE_PAIRS_AND_THE_CMC_REQUEST_OBJECT_"></a> name-value pairs and the CMC request object:</dt>
<dd>
A CMC request object (<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>) contains sequences of <b>TaggedAttribute</b>, <b>TaggedRequest</b>, and <b>TaggedContentInfo</b> ASN.1 structures. For more information,  see <a href="/windows/desktop/SecCertEnroll/cmc-attributes">CMC Attributes</a>


The <b>TaggedAttribute</b> structure can contain a <b>RegInfo</b> attribute. This attribute consists of a byte array that contains the name-value pair collection. The byte array is created in the following manner:<ul>
<li>Each name-value string is standardized. For example, "%5C" escapes are substituted for backslash (\\) characters.</li>
<li>Each name-value pair is concatenated by using an equal sign (=).</li>
<li>All of the pairs are concatenated by using an ampersand (&amp;)between each pair.</li>
<li>The result is encoded as a UTF-8 string.</li>
</ul>


The following example shows the ASN.1 output for a CMC certificate that contains a <b>RegInfo</b> attribute that contains a single name-value pair of "RequesterName=Domain\TargetUser".


``` syntax

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
      72 26                                             ; r&
...

```

</dd>
</dl>

## -inheritance

The <b>IX509NameValuePair</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509NameValuePair</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a>
