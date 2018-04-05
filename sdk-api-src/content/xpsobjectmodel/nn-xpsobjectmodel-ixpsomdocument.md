---
UID: NN:xpsobjectmodel.IXpsOMDocument
title: IXpsOMDocument
author: windows-driver-content
description: An ordered sequence of fixed pages and document-level resources that make up the document.
old-location: xps\ixpsomdocument.htm
old-project: printdocs
ms.assetid: 22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMDocument, IXpsOMDocument interface [XPS Documents and Packaging], IXpsOMDocument interface [XPS Documents and Packaging], described, xps.ixpsomdocument, xpsobjectmodel/IXpsOMDocument
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMDocument
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocument interface


## -description


An ordered sequence of fixed pages and document-level resources that make up the document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMDocument</b> interface inherits from <a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>. <b>IXpsOMDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/372aa8fd-efbb-4196-9137-4a9581c69f6c">GetDocumentStructureResource</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface of the resource that contains structural information about the document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae465c16-9756-4c5d-9601-3087ced9c1f0">GetOwner</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a> interface that contains the document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65e8b20b-6a6b-4d24-86a1-b9d1833caa3c">GetPageReferences</a>
</td>
<td align="left" width="63%">

              Gets the <a href="https://msdn.microsoft.com/4b51bc29-c653-41fa-bbd3-9ff529f84e4e">IXpsOMPageReferenceCollection</a> interface of the document, which allows virtualized access to its pages.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/381bfbb3-1dfd-4761-acdc-cfe64a3aeeb5">GetPrintTicketResource</a>
</td>
<td align="left" width="63%">

              Gets the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface of the document-level print ticket.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87be3040-6113-4876-a847-93620207647f">GetSignatureBlockResources</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/681bdb9c-69dd-4bf6-a4b3-c490f7a0363e">IXpsOMSignatureBlockResourceCollection</a> interface, which refers to a collection of the document's digital signature block resources.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86d62b73-b7a7-4470-9e55-f4eab50531d0">SetDocumentStructureResource</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface for the document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009c2124-c855-4043-9a23-c0313b504853">SetPrintTicketResource</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface for the  document-level print ticket.
            

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMDocument    *newInterface;
IOpcPartUri       *partUri;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreatePartUri(partUriString, &amp;partUri);
    
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory-&gt;CreateDocument (partUri, &amp;newInterface);
        
        if (SUCCEEDED(hr))
        {
            // use newInterface

            newInterface-&gt;Release();
        }
        partUri-&gt;Release();
    }
    xpsFactory-&gt;Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d181c62b-e1a5-45ee-9ffd-85bb6be24892">IXpsOMObjectFactory::CreateDocument</a>



<a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

