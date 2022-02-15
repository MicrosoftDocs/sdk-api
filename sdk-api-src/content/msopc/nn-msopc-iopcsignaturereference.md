---
UID: NN:msopc.IOpcSignatureReference
title: IOpcSignatureReference (msopc.h)
description: Represents a reference to XML markup that has been or will be signed.
helpviewer_keywords: ["IOpcSignatureReference","IOpcSignatureReference interface [Open Packaging Conventions]","IOpcSignatureReference interface [Open Packaging Conventions]","described","msopc/IOpcSignatureReference","opc.iopcsignaturereference"]
old-location: opc\iopcsignaturereference.htm
tech.root: OPC
ms.assetid: 2ce40bc7-754a-4f69-9348-75603e2257a4
ms.date: 12/05/2018
ms.keywords: IOpcSignatureReference, IOpcSignatureReference interface [Open Packaging Conventions], IOpcSignatureReference interface [Open Packaging Conventions],described, msopc/IOpcSignatureReference, opc.iopcsignaturereference
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcSignatureReference
 - msopc/IOpcSignatureReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSignatureReference
---

# IOpcSignatureReference interface


## -description

Represents a reference to XML markup that has been or will be signed. This referenced XML markup is serialized in the signature markup when a signature is generated.

## -inheritance

The <b>IOpcSignatureReference</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureReference</b> also has these types of members:

## -remarks

To create 
				an <b>IOpcSignatureReference</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-create">IOpcSignatureReferenceSet::Create</a> method. <b>IOpcSignatureReferenceSet::Create</b> does not create the reference to the package-specific <b>Object</b> element; that reference is created automatically when the signature is generated.

To access an <b>IOpcSignatureReference</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceenumerator-getcurrent">IOpcSignatureReferenceEnumerator::GetCurrent</a> method. <b>IOpcSignatureReferenceEnumerator::GetCurrent</b> does not access the reference to the package-specific <b>Object</b> element; call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getpackageobjectreference">IOpcDigitalSignature::GetPackageObjectReference</a> method to access that  reference.

The interface provides methods to access information about the reference itself, and referenced XML element. The referenced element can be the package-specific <b>Object</b> element, an application-specific  <b>Object</b> element, or a child element of an application-specific  <b>Object</b>. 

 When a signature is generated, this reference information is serialized in the XML markup of the signature (signature markup).  In signature markup, the information is represented by a  <b>Reference</b> element that has its <b>URI</b> attribute value set to "#" followed by the <b>Id</b> attribute value  of the referenced element. For example, if the <b>Id</b> attribute of the referenced element is "Application" the <b>URI</b> attribute of the <b>Reference</b> element is set to "#Application" as shown in the following markup.

The following signature markup shows a serialized reference to a signed, application-specific <b>Object</b> element.


```xml
<Signature Id="SignatureId" xmlns="http://www.w3.org/2000/09/xmldsig#">
    <SignedInfo>
        [...]
        <Reference URI="#idPackageObject" ...>
            [...]
        </Reference>
        <!-- This reference indicates that the application-specific
        Object element was signed when the signature was generated.-->
        <Reference URI="#Application" ...>
            [...]
        </Reference>
    </SignedInfo>
    [...]
    <Object Id="idPackageObject" ...>
        [...]
    </Object>
    <!-- This application-specific <Object> element was signed when the
    signature was generated. -->
    <Object Id="Application">
        [...]
    </Object>
</Signature>
```


The following signature markup shows a serialized reference to a signed, child element of an application-specific <b>Object</b> element.<div class="alert"><b>Note</b>  More than one child element of an application-specific <b>Object</b> can be referenced for signing.</div>
<div> </div>



```xml
<Signature Id="SignatureId" xmlns="http://www.w3.org/2000/09/xmldsig#">
    <SignedInfo>
        [...]
        <Reference URI="#idPackageObject" ...>
            [...]
        </Reference>
        <!-- This reference indicates that MyElement in the application
        -specific Object element was signed when the signature was
        generated. -->
        <Reference URI="#MyElementId" ...>
            [...]
        </Reference>
    </SignedInfo>
    [...]
    <Object Id="idPackageObject" ...>
        [...]
    </Object>
    <Object Id="Application">
        [...]
            <!-- This element is signed. -->
            <MyElement Id="MyElementId">
                [...]
            </MyElement>
        [...]
    </Object>
</Signature>
```

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
