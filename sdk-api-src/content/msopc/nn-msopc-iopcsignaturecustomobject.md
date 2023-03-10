---
UID: NN:msopc.IOpcSignatureCustomObject
title: IOpcSignatureCustomObject (msopc.h)
description: Represents an application-specific Object element that has been or will be signed.
helpviewer_keywords: ["IOpcSignatureCustomObject","IOpcSignatureCustomObject interface [Open Packaging Conventions]","IOpcSignatureCustomObject interface [Open Packaging Conventions]","described","msopc/IOpcSignatureCustomObject","opc.iopcsignaturecustomobject"]
old-location: opc\iopcsignaturecustomobject.htm
tech.root: OPC
ms.assetid: 4ebb4fbe-66cc-46d9-b548-31177d9f6da9
ms.date: 12/05/2018
ms.keywords: IOpcSignatureCustomObject, IOpcSignatureCustomObject interface [Open Packaging Conventions], IOpcSignatureCustomObject interface [Open Packaging Conventions],described, msopc/IOpcSignatureCustomObject, opc.iopcsignaturecustomobject
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
 - IOpcSignatureCustomObject
 - msopc/IOpcSignatureCustomObject
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
 - IOpcSignatureCustomObject
---

# IOpcSignatureCustomObject interface


## -description

Represents an application-specific <b>Object</b> element that has been or will be signed.

## -inheritance

The <b>IOpcSignatureCustomObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureCustomObject</b> also has these types of members:

## -remarks

An <b>IOpcSignatureCustomObject</b> interface pointer provides access to the XML markup of the <b>Object</b> element it represents. To access the XML markup of the  <b>Object</b> element, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobject-getxml">IOpcSignatureCustomObject::GetXml</a> method.

Serialized application-specific <b>Object</b> elements in signature markup can be added, removed, or modified by replacing the signature markup.

To replace signature markup, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-replacesignaturexml">IOpcDigitalSignatureManager::ReplaceSignatureXml</a> method. The caller must ensure that addition, deletion, or modification of application-specific <b>Object</b> elements does not break the signature.

To sign an application-specific  <b>Object</b> element or a child of the element, create a reference to the element to be signed. Create the reference by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-create">IOpcSignatureReferenceSet::Create</a> method with the <i>referenceUri</i> parameter value set to "#" followed by the <b>Id</b> attribute value  of the referenced element. For example, if the <b>Id</b> attribute of the referenced element is "Application",  set <i>referenceUri</i> to "#Application".

To create an <b>IOpcSignatureCustomObject</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobjectset-create">IOpcSignatureCustomObjectSet::Create</a> method.

To access  an <b>IOpcSignatureCustomObject</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobjectenumerator-getcurrent">IOpcSignatureCustomObjectEnumerator::GetCurrent</a> method.

When a signature is generated, the markup of application-specific <b>Object</b> element is included in the signature markup.

Application-specific <b>Object</b> elements are not required for package signatures.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectenumerator">IOpcSignatureCustomObjectEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
