---
UID: NN:xpsobjectmodel.IXpsOMPageReference
title: IXpsOMPageReference
author: windows-sdk-content
description: Enables virtualization of pages in an XPS document.
old-location: xps\ixpsompagereference.htm
old-project: printdocs
ms.assetid: cdebab24-f918-4235-b4d5-5ee1007ade87
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMPageReference, IXpsOMPageReference interface [XPS Documents and Packaging], IXpsOMPageReference interface [XPS Documents and Packaging],described, xps.ixpsompagereference, xpsobjectmodel/IXpsOMPageReference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPageReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPageReference interface


## -description


Enables virtualization of pages in an XPS document.

A page reference defers loading of the full object model of a page until  the page is requested. If the page has not been altered, it  can also be unloaded on request.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPageReference</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMPageReference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPageReference</b> interface has these methods.
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
<a href="https://msdn.microsoft.com/82c64e8a-d8fb-41e3-95f8-b8ca490eae78">CollectLinkTargets</a>
</td>
<td align="left" width="63%">

              Gets an  <a href="https://msdn.microsoft.com/b27f83fc-0fcf-44e9-a6ce-c3612c5399ff">IXpsOMNameCollection</a> interface that contains the names of all the document sub-tree objects whose  <b>IsHyperlinkTarget</b> property is set to <b>true</b>.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52a45351-669c-42f3-b02b-afbf42727313">CollectPartResources</a>
</td>
<td align="left" width="63%">
Creates a list of all part-based resources that are associated with the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/430b9169-7fc5-493d-85a8-dddf46dfef8f">DiscardPage</a>
</td>
<td align="left" width="63%">
Discards the page from memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e25d910-5ca5-4e92-8b77-479c48a0089a">GetAdvisoryPageDimensions</a>
</td>
<td align="left" width="63%">
Gets the suggested dimensions of the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1229972d-ae0f-41db-aafb-99d9647360e1">GetOwner</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface that contains the page reference.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0004217f-f379-4175-bbce-eea93d96f37f">GetPage</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface that contains the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a205f18c-f8dd-4241-b1fd-b6505fb5bad9">GetPrintTicketResource</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the  <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface of the page-level print ticket resource that is associated with the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b768734-07e3-4917-adb9-29989e7e2b32">GetStoryFragmentsResource</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the  <a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a> interface of the StoryFragments part resource that is associated with the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec9cc698-892f-4216-b491-cabdfa60deaa">GetThumbnailResource</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface of the  thumbnail image resource that is associated with the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/721dffd7-a15f-4028-be9e-854a4445d76d">HasRestrictedFonts</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the document sub-tree of the referenced page includes any Glyphs that have a font resource whose  <b>EmbeddingOption</b> property is set to <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12b7d824-65eb-4d24-bfb6-40f55085186c">IsPageLoaded</a>
</td>
<td align="left" width="63%">
Gets the referenced page status,  which indicates whether the  page is loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8286fd78-a7d8-4bf4-9b08-b93e19abccf9">SetAdvisoryPageDimensions</a>
</td>
<td align="left" width="63%">
Sets the suggested dimensions of the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d1381ad-6ac8-4ea4-99a2-8bc5d95773c7">SetPage</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface of the page reference.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76594c7d-327d-45a5-8947-c587ada7b758">SetPrintTicketResource</a>
</td>
<td align="left" width="63%">

              Sets  the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface pointer of the page-level print ticket resource that is to be assigned to the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e096e8f-d2f1-4dcb-9a86-c56ff53393d1">SetStoryFragmentsResource</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a> interface pointer of the StoryFragments resource to be assigned to the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b44c041d-dccd-4b64-b85b-454b203b865b">SetThumbnailResource</a>
</td>
<td align="left" width="63%">

              Sets the pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface of the thumbnail image resource to be assigned to the page.
            

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
IXpsOMPageReference    *newInterface;
// The following value is defined outside of 
// this example.
XPS_SIZE        advisoryPageDimensions;

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
    hr = xpsFactory-&gt;CreatePageReference (
        &amp;advisoryPageDimensions,
        &amp;newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface-&gt;Release();
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
For information about using this interface in a program, see <a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a> and <a href="https://msdn.microsoft.com/90b726aa-29da-4cfb-9c69-f471c2acb678">Navigate the XPS OM</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a>



<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/b27f83fc-0fcf-44e9-a6ce-c3612c5399ff">IXpsOMNameCollection</a>



<a href="https://msdn.microsoft.com/037a7926-def4-4be3-b7c5-3c4c588e75ae">IXpsOMObjectFactory::CreatePageReference</a>



<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a>



<a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/90b726aa-29da-4cfb-9c69-f471c2acb678">Navigate the XPS OM</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

