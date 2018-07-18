---
UID: NN:xpsobjectmodel.IXpsOMFontResource
title: IXpsOMFontResource
author: windows-sdk-content
description: Provides an IStream interface to a font resource.
old-location: xps\ixpsomfontresource.htm
old-project: printdocs
ms.assetid: dd0ce1c0-1c04-46a8-9075-93de9b3e3062
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMFontResource, IXpsOMFontResource interface [XPS Documents and Packaging], IXpsOMFontResource interface [XPS Documents and Packaging],described, xps.ixpsomfontresource, xpsobjectmodel/IXpsOMFontResource
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
 - IXpsOMFontResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMFontResource interface


## -description


Provides an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to a font resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMFontResource</b> interface inherits from <a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>. <b>IXpsOMFontResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMFontResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c4b3741-2c9c-4964-ae51-53dd738e8d9b">GetEmbeddingOption</a>
</td>
<td align="left" width="63%">
Gets the embedding option that will be applied when the resource is serialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d512e862-e2d0-4cc8-a20a-bc3cfbfbcc47">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87a9d003-9406-4c94-b814-4986d213ee47">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be associated with this resource.

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
IXpsOMFontResource    *newInterface;
IOpcPartUri           *partUri;

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
    // The partUriString and acquiredStream variables 
    //   are defined outside of this example.
    hr = xpsFactory-&gt;CreatePartUri(partUriString, &amp;partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory-&gt;CreateFontResource (
            acquiredStream, 
            XPS_FONT_EMBEDDING_NORMAL,    // normal
            partUri, 
            FALSE,                        // not obfuscated
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



## -see-also




<a href="https://msdn.microsoft.com/9893716b-5004-4886-9bed-49a447e97f42">IXpsOMObjectFactory::CreateFontResource</a>



<a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

