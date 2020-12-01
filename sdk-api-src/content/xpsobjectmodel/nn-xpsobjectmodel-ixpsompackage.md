---
UID: NN:xpsobjectmodel.IXpsOMPackage
title: IXpsOMPackage (xpsobjectmodel.h)
description: Provides the top-level entry into the XPS object model tree.
helpviewer_keywords: ["IXpsOMPackage","IXpsOMPackage interface [XPS Documents and Packaging]","IXpsOMPackage interface [XPS Documents and Packaging]","described","xps.ixpsompackage","xpsobjectmodel/IXpsOMPackage"]
old-location: xps\ixpsompackage.htm
tech.root: xps
ms.assetid: 7b0a36d6-1af1-4c2c-af14-d6139e9115c3
ms.date: 12/05/2018
ms.keywords: IXpsOMPackage, IXpsOMPackage interface [XPS Documents and Packaging], IXpsOMPackage interface [XPS Documents and Packaging],described, xps.ixpsompackage, xpsobjectmodel/IXpsOMPackage
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - IXpsOMPackage
 - xpsobjectmodel/IXpsOMPackage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPackage
---

# IXpsOMPackage interface


## -description

Provides the top-level entry into the XPS object model tree.

 Although this interface does not correspond to any XPS markup, it does correspond to the XPS document, and it is required to save the components of an XPS object model tree as an XPS document.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPackage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMPackage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPackage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getcoreproperties">GetCoreProperties</a>
</td>
<td align="left" width="63%">
Gets a pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdiscardcontrolpartname">GetDiscardControlPartName</a>
</td>
<td align="left" width="63%">
Gets the name of the discard control part in the XPS package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdocumentsequence">GetDocumentSequence</a>
</td>
<td align="left" width="63%">
Gets a pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface that contains the document sequence of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getthumbnailresource">GetThumbnailResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface of the thumbnail resource that is associated with the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-setcoreproperties">SetCoreProperties</a>
</td>
<td align="left" width="63%">
Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-setdiscardcontrolpartname">SetDiscardControlPartName</a>
</td>
<td align="left" width="63%">
Sets the name of the discard control part in the XPS package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-setdocumentsequence">SetDocumentSequence</a>
</td>
<td align="left" width="63%">
Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-setthumbnailresource">SetThumbnailResource</a>
</td>
<td align="left" width="63%">
Sets the thumbnail image of the XPS document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile">WriteToFile</a>
</td>
<td align="left" width="63%">
Writes the XPS package to a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream">WriteToStream</a>
</td>
<td align="left" width="63%">
Writes the XPS package to a specified stream.

</td>
</tr>
</table>

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPackage    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
      __uuidof(XpsOMObjectFactory),
      NULL, 
      CLSCTX_INPROC_SERVER,
      __uuidof(IXpsOMObjectFactory),
      reinterpret_cast<LPVOID*>(&xpsFactory)
      );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreatePackage (&newInterface);
    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface->Release();
    }

    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```


For information about using this interface in a program, see <a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackage">IXpsOMObjectFactory::CreatePackage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile">IXpsOMObjectFactory::CreatePackageFromFile</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream">IXpsOMObjectFactory::CreatePackageFromStream</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>