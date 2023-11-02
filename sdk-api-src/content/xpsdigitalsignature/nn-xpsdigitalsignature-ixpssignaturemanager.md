---
UID: NN:xpsdigitalsignature.IXpsSignatureManager
title: IXpsSignatureManager (xpsdigitalsignature.h)
description: Manages the digital signatures and digital signature requests of an XPS document.
helpviewer_keywords: ["IXpsSignatureManager","IXpsSignatureManager interface [XPS Documents and Packaging]","IXpsSignatureManager interface [XPS Documents and Packaging]","described","xps.ixpssignaturemanager","xpsdigitalsignature/IXpsSignatureManager"]
old-location: xps\ixpssignaturemanager.htm
tech.root: xps
ms.assetid: 31283ebe-91f4-42be-9a9b-6fcd641dc356
ms.date: 12/05/2018
ms.keywords: IXpsSignatureManager, IXpsSignatureManager interface [XPS Documents and Packaging], IXpsSignatureManager interface [XPS Documents and Packaging],described, xps.ixpssignaturemanager, xpsdigitalsignature/IXpsSignatureManager
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - IXpsSignatureManager
 - xpsdigitalsignature/IXpsSignatureManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager
---

# IXpsSignatureManager interface

## -description

Manages the digital signatures and digital signature requests of an XPS document.

## -inheritance

The <b>IXpsSignatureManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSignatureManager</b> also has these types of members:

## -members

The <b>IXpsSignatureManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock">AddSignatureBlock</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface and adds it to the signature block collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">CreateSigningOptions</a>
</td>
<td align="left" width="63%">
Creates a new  <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatureblocks">GetSignatureBlocks</a>
</td>
<td align="left" width="63%">
Gets a pointer to an  <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a> interface that contains a collection of signature blocks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatureoriginpartname">GetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the signature origin part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures">GetSignatures</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection">IXpsSignatureCollection</a> interface that contains a collection of XPS digital signatures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a>
</td>
<td align="left" width="63%">
Loads an existing XPS package from a file into the digital signature manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a>
</td>
<td align="left" width="63%">
Loads an XPS package from a stream into the digital signature manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-savepackagetofile">SavePackageToFile</a>
</td>
<td align="left" width="63%">
Saves the XPS package to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-savepackagetostream">SavePackageToStream</a>
</td>
<td align="left" width="63%">
Saves the XPS package by writing it to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-setsignatureoriginpartname">SetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the signature origin part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a>
</td>
<td align="left" width="63%">
Signs the contents of an  XPS package as specified by the signing options and returns the resulting digital signature.

</td>
</tr>
</table>

## -members

The <b>IXpsSignatureManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock">AddSignatureBlock</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface and adds it to the signature block collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">CreateSigningOptions</a>
</td>
<td align="left" width="63%">
Creates a new  <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatureblocks">GetSignatureBlocks</a>
</td>
<td align="left" width="63%">
Gets a pointer to an  <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a> interface that contains a collection of signature blocks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatureoriginpartname">GetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the signature origin part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures">GetSignatures</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection">IXpsSignatureCollection</a> interface that contains a collection of XPS digital signatures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a>
</td>
<td align="left" width="63%">
Loads an existing XPS package from a file into the digital signature manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a>
</td>
<td align="left" width="63%">
Loads an XPS package from a stream into the digital signature manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-savepackagetofile">SavePackageToFile</a>
</td>
<td align="left" width="63%">
Saves the XPS package to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-savepackagetostream">SavePackageToStream</a>
</td>
<td align="left" width="63%">
Saves the XPS package by writing it to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-setsignatureoriginpartname">SetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the signature origin part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a>
</td>
<td align="left" width="63%">
Signs the contents of an  XPS package as specified by the signing options and returns the resulting digital signature.

</td>
</tr>
</table>

## -remarks

To initialize the signature manager for use with an XPS document, instantiate an <b>IXpsSignatureManager</b> interface by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> as shown in the following example.

```cpp

IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them
    newInterface->Release();
}

```


The interface instantiated by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> can be used by only one XPS document, which must be loaded by calling <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a> or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a> before
calling any other method.

After the <b>IXpsSignatureManager</b> interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
