---
UID: NN:xpsobjectmodel.IXpsOMPartResources
title: IXpsOMPartResources
author: windows-sdk-content
description: Provides access to all shared, part-based resources of the XPS document.
old-location: xps\ixpsompartresources.htm
old-project: printdocs
ms.assetid: 9f706f23-25a0-40ee-93f4-3d7ac98ad6ed
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IXpsOMPartResources, IXpsOMPartResources interface [XPS Documents and Packaging], IXpsOMPartResources interface [XPS Documents and Packaging],described, xps.ixpsompartresources, xpsobjectmodel/IXpsOMPartResources
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
 - IXpsOMPartResources
product: Windows
targetos: Windows
req.lib: XpsPrint.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPartResources interface


## -description


Provides access to all shared, part-based resources of the XPS document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPartResources</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMPartResources</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPartResources</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad986a95-a77d-4e04-b857-09ee137070e2">GetColorProfileResources</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/cb9253f3-461e-47a3-820b-bb6bf5e30210">IXpsOMColorProfileResourceCollection</a> interface that contains  the color profiles that are used in the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6655eed-5dd2-4b36-9ed7-55a3b25940e9">GetFontResources</a>
</td>
<td align="left" width="63%">
Gets the   <a href="https://msdn.microsoft.com/71153c4c-631b-4f7a-9dd5-8537dcaca150">IXpsOMFontResourceCollection</a> interface that contains the fonts that are used in the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d30281b7-0b2c-4240-813b-a53c8acb819c">GetImageResources</a>
</td>
<td align="left" width="63%">
Gets the  <a href="https://msdn.microsoft.com/aed8b23e-71fd-49e6-aae9-006a59e0111b">IXpsOMImageResourceCollection</a> interface that contains the images that are used in the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb12fe80-9e94-4797-adf5-a1986512bf57">GetRemoteDictionaryResources</a>
</td>
<td align="left" width="63%">
Gets the  <a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a> interface that contains the remote resource dictionaries  that are used in the XPS document.
            

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
IXpsOMPartResources    *newInterface;

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
    hr = xpsFactory-&gt;CreatePartResources (&amp;newInterface);

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



## -see-also




<a href="https://msdn.microsoft.com/f525139b-a94f-41ee-966f-408079a9e676">IXpsOMObjectFactory::CreatePartResources</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

