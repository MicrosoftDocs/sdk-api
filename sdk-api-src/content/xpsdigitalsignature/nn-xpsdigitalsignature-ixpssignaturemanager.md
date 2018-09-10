---
UID: NN:xpsdigitalsignature.IXpsSignatureManager
title: IXpsSignatureManager
author: windows-sdk-content
description: Manages the digital signatures and digital signature requests of an XPS document.
old-location: xps\ixpssignaturemanager.htm
tech.root: printdocs
ms.assetid: 31283ebe-91f4-42be-9a9b-6fcd641dc356
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsSignatureManager, IXpsSignatureManager interface [XPS Documents and Packaging], IXpsSignatureManager interface [XPS Documents and Packaging],described, xps.ixpssignaturemanager, xpsdigitalsignature/IXpsSignatureManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureManager interface


## -description


Manages the digital signatures and digital signature requests of an XPS document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsSignatureManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsSignatureManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsSignatureManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a299882f-b9f4-4297-8438-e92d148a4014">AddSignatureBlock</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface and adds it to the signature block collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f64f46a-905a-48cf-9e7a-f6cc1b2d6450">CreateSigningOptions</a>
</td>
<td align="left" width="63%">
Creates a new  <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f7ba22f-7c3b-47bf-8cb5-2e4e4a548dc2">GetSignatureBlocks</a>
</td>
<td align="left" width="63%">
Gets a pointer to an  <a href="https://msdn.microsoft.com/e8f7be84-389e-40cf-a093-83417ba184c7">IXpsSignatureBlockCollection</a> interface that contains a collection of signature blocks.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d70e6bc-1101-40fa-b91c-69facc3ca195">GetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the signature origin part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a6a9a10-bc1d-45b8-a1b9-c7b725d9c13b">GetSignatures</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/b8c46cc0-e071-4016-b658-1a5cd554a4c9">IXpsSignatureCollection</a> interface that contains a collection of XPS digital signatures.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecb33eee-4622-4a2e-bc24-7a77d16ef4a4">LoadPackageFile</a>
</td>
<td align="left" width="63%">
Loads an existing XPS package from a file into the digital signature manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/755bbd41-0941-4956-a99d-45b39f9b030f">LoadPackageStream</a>
</td>
<td align="left" width="63%">
Loads an XPS package from a stream into the digital signature manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/954d8eb1-8680-410b-909b-da7a6572c0f3">SavePackageToFile</a>
</td>
<td align="left" width="63%">
Saves the XPS package to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a29c8e2-2e5d-4cc0-adfd-6debabca9243">SavePackageToStream</a>
</td>
<td align="left" width="63%">
Saves the XPS package by writing it to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/686f31e1-3c61-449d-91f7-67f72d88a4b7">SetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the signature origin part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82a57ca8-edc7-4248-92d1-8092f6dce4f8">Sign</a>
</td>
<td align="left" width="63%">
Signs the contents of an  XPS package as specified by the signing options and returns the resulting digital signature.

</td>
</tr>
</table> 


## -remarks



To initialize the signature manager for use with an XPS document, instantiate an <b>IXpsSignatureManager</b> interface by calling <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> as shown in the following example.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast&lt;LPVOID*&gt;(&amp;newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface-&gt;LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface-&gt;Release();
}    
</pre>
</td>
</tr>
</table></span></div>
The interface instantiated by <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> can be used by only one XPS document, which must be loaded by calling <a href="https://msdn.microsoft.com/ecb33eee-4622-4a2e-bc24-7a77d16ef4a4">LoadPackageFile</a> or <a href="https://msdn.microsoft.com/755bbd41-0941-4956-a99d-45b39f9b030f">LoadPackageStream</a> before
calling any other method.

After the <b>IXpsSignatureManager</b> interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

