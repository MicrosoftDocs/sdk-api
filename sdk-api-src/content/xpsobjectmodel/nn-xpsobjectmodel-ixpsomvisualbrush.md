---
UID: NN:xpsobjectmodel.IXpsOMVisualBrush
title: IXpsOMVisualBrush
author: windows-sdk-content
description: A brush that uses a visual element as a source.
old-location: xps\ixpsomvisualbrush.htm
tech.root: printdocs
ms.assetid: 56c11e64-64a8-4c42-9547-4f1fcdc13a4b
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMVisualBrush, IXpsOMVisualBrush interface [XPS Documents and Packaging], IXpsOMVisualBrush interface [XPS Documents and Packaging],described, xps.ixpsomvisualbrush, xpsobjectmodel/IXpsOMVisualBrush
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
 - IXpsOMVisualBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisualBrush interface


## -description


A brush that uses a visual element as a source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMVisualBrush</b> interface inherits from <a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>. <b>IXpsOMVisualBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMVisualBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3341566-6b35-4ed9-9db8-d5493656755e">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8fb6698-8ce7-42a1-bad6-bde3d5dbbbf8">GetVisual</a>
</td>
<td align="left" width="63%">
Gets a pointer to the interface of the resolved visual to be used as the source for the brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a75c2bca-eaac-4382-9211-fbc1b05f1414">GetVisualLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the interface of the local, unshared visual used as the source for the brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/091cb7f3-6302-40a0-b509-c72e20109f75">GetVisualLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key name of a visual in a resource dictionary; the visual is to be used as the source for the brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ef37838-ff5f-4c8f-9fa3-30d11417c09d">SetVisualLocal</a>
</td>
<td align="left" width="63%">
Sets the interface pointer of the local, unshared visual used as the source for the brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of the shared visual, which is stored in a resource dictionary, to be used as the source for the brush.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMVisualBrush        *newInterface;

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
    hr = xpsFactory->CreateVisualBrush (
        &viewBox,
        &viewPort,
        &newInterface);

    if (SUCCEEDED(hr))
    {
        // assign visual using one of the following:
        newInterface->SetVisualLocal (localVisual);
        // or
        newInterface->SetVisualLookup (visualLookupKey);
        // use newInterface

        newInterface->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
// use newInterface

newInterface->Release();
xpsFactory->Release();


```





## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="https://msdn.microsoft.com/ad19841a-629f-4127-a6ea-890168e0c53c">IXpsOMObjectFactory::CreateVisualBrush</a>



<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

