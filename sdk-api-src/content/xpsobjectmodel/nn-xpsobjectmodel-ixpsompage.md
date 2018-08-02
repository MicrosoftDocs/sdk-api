---
UID: NN:xpsobjectmodel.IXpsOMPage
title: IXpsOMPage
author: windows-sdk-content
description: Provides the root node of a tree of objects that hold the contents of a single page.
old-location: xps\ixpsompage.htm
old-project: printdocs
ms.assetid: 741deebd-9dce-4cd9-883e-4586c10a4609
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IXpsOMPage, IXpsOMPage interface [XPS Documents and Packaging], IXpsOMPage interface [XPS Documents and Packaging],described, xps.ixpsompage, xpsobjectmodel/IXpsOMPage
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
 - IXpsOMPage
product: Windows
targetos: Windows
req.lib: XpsPrint.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPage interface


## -description


Provides the root node of a tree of objects that hold the contents of  a single page. 

The <b>IXpsOMPage</b> interface corresponds to the <b>FixedPage</b> element in XPS document markup.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPage</b> interface inherits from <a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>. <b>IXpsOMPage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79599ede-fd81-4d1a-b71b-ac5742e384ca">GenerateUnusedLookupKey</a>
</td>
<td align="left" width="63%">
Generates a unique name that can be used as a lookup key by a resource in a resource dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ce82a0e-b01c-4c1e-8907-31f51dc51f10">GetBleedBox</a>
</td>
<td align="left" width="63%">
Gets the dimensions of the page's bleed box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6402bcd0-84cb-472f-8c3c-1fe34eecc6d2">GetContentBox</a>
</td>
<td align="left" width="63%">
Gets the dimensions of the page's content box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e842c828-6e8c-4190-b845-8c8a26af1579">GetDictionary</a>
</td>
<td align="left" width="63%">
Gets a pointer to the resolved <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface that is associated with this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eece7d5-2f2d-4fae-a2f4-8e52236f57c4">GetDictionaryLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the local, unshared dictionary that is associated with this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12313d19-e6f1-4ec3-9702-2a403087763a">GetDictionaryResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface of the shared dictionary resource that is used by this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/172636d5-c375-4552-97a8-d874b6aa4843">GetIsHyperlinkTarget</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the page is the target of a hyperlink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d16378cc-dd1c-49f9-9c1b-1eb0d78067f7">GetLanguage</a>
</td>
<td align="left" width="63%">
Gets the <b>Language</b> property of the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c133dce-3a5a-4d7f-af83-2e185450c207">GetName</a>
</td>
<td align="left" width="63%">
Gets the <b>Name</b> property of the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd29eaa7-8f9c-4468-ad3b-a159bf5f516c">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface that contains the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24a81c7a-f048-4347-8023-96ed85bec2a1">GetPageDimensions</a>
</td>
<td align="left" width="63%">
Gets the page dimensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8181513f-2a5d-4b43-aa40-7f886a8af7f7">GetVisuals</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/f373b437-3973-40aa-9cac-a6b196a3e5d1">IXpsOMVisualCollection</a> interface that contains a collection  of the page's visual objects.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/947313e1-6c95-4751-997f-d5172acaa5d5">SetBleedBox</a>
</td>
<td align="left" width="63%">
Sets the dimensions of the page's bleed box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5262ce99-8112-4f4f-a173-5927341b4a2e">SetContentBox</a>
</td>
<td align="left" width="63%">
Sets the dimensions of the page's content box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface pointer of the page's local dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e424c70e-289c-4519-8b20-5fb98d46bf34">SetDictionaryResource</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer of the page's remote dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8096303-5940-4ad1-aa5a-de604efe8c9e">SetIsHyperlinkTarget</a>
</td>
<td align="left" width="63%">
Specifies whether the page is the target of a hyperlink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bf0c7ed-84fc-45c0-8058-b833c3913f09">SetLanguage</a>
</td>
<td align="left" width="63%">
Sets the <b>Language</b> property of the page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/675e4fd2-e8b9-400f-9042-df5b0bb0b89a">SetName</a>
</td>
<td align="left" width="63%">
Sets the <b>Name</b> property of this page.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ae0a584-afa2-4288-82f8-c52c46de390f">SetPageDimensions</a>
</td>
<td align="left" width="63%">
Sets dimensions of the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a>
</td>
<td align="left" width="63%">
Writes the page to the specified stream.

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
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreatePartUri(partUriString, &amp;partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory-&gt;CreatePage (
            &amp;pageDimensions,
            language,
            partUri,
            &amp;newInterface);

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
For information about using this interface in a program, see <a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a> and <a href="https://msdn.microsoft.com/90b726aa-29da-4cfb-9c69-f471c2acb678">Navigate the XPS OM</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a>



<a href="https://msdn.microsoft.com/9212ccd8-0793-40cc-bab5-609ea74715f7">IXpsOMObjectFactory::CreatePage</a>



<a href="https://msdn.microsoft.com/daeafc73-33b0-4c88-b92d-da4ca42b19a9">IXpsOMObjectFactory::CreatePageFromStream</a>



<a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/90b726aa-29da-4cfb-9c69-f471c2acb678">Navigate the XPS OM</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

