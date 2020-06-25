---
UID: NN:msopc.IOpcSignatureCustomObjectSet
title: IOpcSignatureCustomObjectSet (msopc.h)
description: An unordered set of IOpcSignatureCustomObject interface pointers that contain the XML markup of application-specific Object elements.
helpviewer_keywords: ["IOpcSignatureCustomObjectSet","IOpcSignatureCustomObjectSet interface [Open Packaging Conventions]","IOpcSignatureCustomObjectSet interface [Open Packaging Conventions]","described","msopc/IOpcSignatureCustomObjectSet","opc.iopcsignaturecustomobjectset"]
old-location: opc\iopcsignaturecustomobjectset.htm
tech.root: OPC
ms.assetid: eb2a561d-2723-45dc-98a6-ecf11101016b
ms.date: 12/05/2018
ms.keywords: IOpcSignatureCustomObjectSet, IOpcSignatureCustomObjectSet interface [Open Packaging Conventions], IOpcSignatureCustomObjectSet interface [Open Packaging Conventions],described, msopc/IOpcSignatureCustomObjectSet, opc.iopcsignaturecustomobjectset
f1_keywords:
- msopc/IOpcSignatureCustomObjectSet
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msopc.h
api_name:
- IOpcSignatureCustomObjectSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcSignatureCustomObjectSet interface


## -description


An unordered set of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointers that contain the XML markup of application-specific <b>Object</b> elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureCustomObjectSet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureCustomObjectSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureCustomObjectSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobjectset-create">Create</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer to represent an application-specific <b>Object</b> element in the signature, and adds the new interface to the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobjectset-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes a specified <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer from the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobjectset-getenumerator">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointers in the set.
            

</td>
</tr>
</table> 


## -remarks



An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer provides access to the XML markup of the <b>Object</b> element it represents. To access the XML markup of the  <b>Object</b> element, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobject-getxml">IOpcSignatureCustomObject::GetXml</a> method.

When an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer is created and added to the set, the <b>Object</b>  it represents is saved when the package is saved.

When an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer is deleted from the set, the <b>Object</b> it represents is not saved when the package is saved.

To create an <b>IOpcSignatureCustomObjectSet</b> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomobjectset">IOpcSigningOptions::GetCustomObjectSet</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

