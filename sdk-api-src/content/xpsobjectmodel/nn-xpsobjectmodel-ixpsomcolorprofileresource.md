---
UID: NN:xpsobjectmodel.IXpsOMColorProfileResource
title: IXpsOMColorProfileResource
author: windows-sdk-content
description: Provides an IStream interface to a color profile resource.
old-location: xps\ixpsomcolorprofileresource.htm
tech.root: printdocs
ms.assetid: 8a344300-c3fc-4225-bfa5-d5d33798a094
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IXpsOMColorProfileResource, IXpsOMColorProfileResource interface [XPS Documents and Packaging], IXpsOMColorProfileResource interface [XPS Documents and Packaging],described, xps.ixpsomcolorprofileresource, xpsobjectmodel/IXpsOMColorProfileResource
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
 - IXpsOMColorProfileResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMColorProfileResource interface


## -description


Provides an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to a color profile resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMColorProfileResource</b> interface inherits from <a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>. <b>IXpsOMColorProfileResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMColorProfileResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bc8bae0-eae7-47bd-a6ac-50ff9bdc2703">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d93ae074-6565-45ea-bc0e-e8401b7d5b47">SetContent</a>
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
IXpsOMColorProfileResource    *newInterface;
IOpcPartUri                   *partUri;

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
    hr = xpsFactory-&gt;CreatePartUri(
        partUriString, 
        &amp;partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory-&gt;CreateColorProfileResource (
            acquiredStream, 
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



## -see-also




<a href="https://msdn.microsoft.com/cb4d1b49-fda6-46c3-a72a-21affdb7e82e">IXpsOMObjectFactory::CreateColorProfileResource</a>



<a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

