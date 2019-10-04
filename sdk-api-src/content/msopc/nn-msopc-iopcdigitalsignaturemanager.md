---
UID: NN:msopc.IOpcDigitalSignatureManager
title: IOpcDigitalSignatureManager (msopc.h)
author: windows-sdk-content
description: Provides access to Packaging Digital Signature Interfaces for a package that is represented by Packaging API objects.
old-location: opc\iopcdigitalsignaturemanager.htm
tech.root: OPC
ms.assetid: 13e8a7b9-1d25-421b-bc81-adc495e6d9c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignatureManager, IOpcDigitalSignatureManager interface [Open Packaging Conventions], IOpcDigitalSignatureManager interface [Open Packaging Conventions],described, msopc/IOpcDigitalSignatureManager, opc.iopcdigitalsignaturemanager
ms.topic: interface
f1_keywords: 
 - "msopc/IOpcDigitalSignatureManager"
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
 - IOpcDigitalSignatureManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcDigitalSignatureManager interface


## -description


Provides access to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a> for a package that is represented by Packaging API objects. These interface methods are called to generate  a signature, or to access and validate existing signatures in the package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcDigitalSignatureManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcDigitalSignatureManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcDigitalSignatureManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-createsigningoptions">CreateSigningOptions</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-getsignatureenumerator">GetSignatureEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointers, which represent package signatures.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-getsignatureoriginpartname">GetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the part name of the Digital Signature Origin part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-removesignature">RemoveSignature</a>
</td>
<td align="left" width="63%">
Removes from the package a specified signature part  that stores signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-replacesignaturexml">ReplaceSignatureXml</a>
</td>
<td align="left" width="63%">
Replaces the existing signature markup that is stored in a specified signature part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-setsignatureoriginpartname">SetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the Digital Signature Origin part to the name represented by a specified <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">Sign</a>
</td>
<td align="left" width="63%">
Signs the package by generating a signature by using the specified certificate and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-validate">Validate</a>
</td>
<td align="left" width="63%">
Validates a specified package signature using a specified certificate.
            

</td>
</tr>
</table> 


## -remarks



 Before the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">Sign</a> method is called to generate a signature, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">IOpcSigningOptions::SetDefaultDigestMethod</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturemethod">IOpcSigningOptions::SetSignatureMethod</a> methods must be called.

To create an   <b>IOpcDigitalSignatureManager</b> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createdigitalsignaturemanager">IOpcFactory::CreateDigitalSignatureManager</a> method.

<div class="alert"><b>Important</b>  If the package is modified while the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">Sign</a> method is being executed, the method may fail or generate an inconsistent signature. To avoid corruption of the package, use the APIs to save the package prior to calling <b>Sign</b>. For information about how to save a package, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/saving-a-package">Saving a Package</a>.</div>
<div> </div>
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-validate">Validate</a> method checks that the specified signature (signed entities and the signature markup) has not been altered since the signature was generated, but does not validate the identity of the signer. <div class="alert"><b>Important</b>  The caller must validate the identity of the signer.</div>
<div> </div>



#### Thread Safety

Packaging objects are not thread-safe.

IOpcSigningOptions
For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignatureenumerator">IOpcDigitalSignatureEnumerator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

