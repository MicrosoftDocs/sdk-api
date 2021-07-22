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



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>
