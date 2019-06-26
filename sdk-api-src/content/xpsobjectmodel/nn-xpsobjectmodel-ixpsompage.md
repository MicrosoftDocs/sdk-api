---
UID: NN:xpsobjectmodel.IXpsOMPage
title: IXpsOMPage (xpsobjectmodel.h)
author: windows-sdk-content
description: Provides the root node of a tree of objects that hold the contents of a single page.
old-location: xps\ixpsompage.htm
tech.root: printdocs
ms.assetid: 741deebd-9dce-4cd9-883e-4586c10a4609
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPage, IXpsOMPage interface [XPS Documents and Packaging], IXpsOMPage interface [XPS Documents and Packaging],described, xps.ixpsompage, xpsobjectmodel/IXpsOMPage
ms.topic: interface
f1_keywords: 
 - "xpsobjectmodel/IXpsOMPage"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPage interface


## -description


Provides the root node of a tree of objects that hold the contents of  a single page. 

The <b>IXpsOMPage</b> interface corresponds to the <b>FixedPage</b> element in XPS document markup.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPage</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>. <b>IXpsOMPage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-generateunusedlookupkey">GenerateUnusedLookupKey</a>
</td>
<td align="left" width="63%">
Generates a unique name that can be used as a lookup key by a resource in a resource dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getbleedbox">GetBleedBox</a>
</td>
<td align="left" width="63%">
Gets the dimensions of the page's bleed box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getcontentbox">GetContentBox</a>
</td>
<td align="left" width="63%">
Gets the dimensions of the page's content box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionary">GetDictionary</a>
</td>
<td align="left" width="63%">
Gets a pointer to the resolved <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface that is associated with this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionarylocal">GetDictionaryLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the local, unshared dictionary that is associated with this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionaryresource">GetDictionaryResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface of the shared dictionary resource that is used by this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getishyperlinktarget">GetIsHyperlinkTarget</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the page is the target of a hyperlink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getlanguage">GetLanguage</a>
</td>
<td align="left" width="63%">
Gets the <b>Language</b> property of the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the <b>Name</b> property of the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getowner">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a> interface that contains the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getpagedimensions">GetPageDimensions</a>
</td>
<td align="left" width="63%">
Gets the page dimensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getvisuals">GetVisuals</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection">IXpsOMVisualCollection</a> interface that contains a collection  of the page's visual objects.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setbleedbox">SetBleedBox</a>
</td>
<td align="left" width="63%">
Sets the dimensions of the page's bleed box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setcontentbox">SetContentBox</a>
</td>
<td align="left" width="63%">
Sets the dimensions of the page's content box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface pointer of the page's local dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer of the page's remote dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setishyperlinktarget">SetIsHyperlinkTarget</a>
</td>
<td align="left" width="63%">
Specifies whether the page is the target of a hyperlink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setlanguage">SetLanguage</a>
</td>
<td align="left" width="63%">
Sets the <b>Language</b> property of the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setname">SetName</a>
</td>
<td align="left" width="63%">
Sets the <b>Name</b> property of this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setpagedimensions">SetPageDimensions</a>
</td>
<td align="left" width="63%">
Sets dimensions of the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-write">Write</a>
</td>
<td align="left" width="63%">
Writes the page to the specified stream.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPage        *newInterface;
// The following values are defined outside of 
// this example.
//  LPWSTR        language;
//  XPS_SIZE      pageDimensions;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast<LPVOID*>(&xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreatePartUri(partUriString, &partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory->CreatePage (
            &pageDimensions,
            language,
            partUri,
            &newInterface);

        if (SUCCEEDED(hr))
        {
            // use newInterface

            newInterface->Release();
        }
        partUri->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```


For information about using this interface in a program, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpage">IXpsOMObjectFactory::CreatePage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpagefromstream">IXpsOMObjectFactory::CreatePageFromStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

