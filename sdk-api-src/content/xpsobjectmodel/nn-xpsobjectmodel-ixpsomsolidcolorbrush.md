---
UID: NN:xpsobjectmodel.IXpsOMSolidColorBrush
title: IXpsOMSolidColorBrush
author: windows-sdk-content
description: A single-color brush.
old-location: xps\ixpsomsolidcolorbrush.htm
tech.root: printdocs
ms.assetid: 26580a25-09d1-4a9b-85c3-aa8ddcc97867
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMSolidColorBrush, IXpsOMSolidColorBrush interface [XPS Documents and Packaging], IXpsOMSolidColorBrush interface [XPS Documents and Packaging],described, xps.ixpsomsolidcolorbrush, xpsobjectmodel/IXpsOMSolidColorBrush
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
 - IXpsOMSolidColorBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMSolidColorBrush interface


## -description


A  single-color brush.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMSolidColorBrush</b> interface inherits from <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>. <b>IXpsOMSolidColorBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMSolidColorBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f25d5cf-b53d-4e86-ae61-1d0c9afc6236">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07201e3d-af2f-4b85-ac03-2911c33f348b">GetColor</a>
</td>
<td align="left" width="63%">
Gets the color value and color profile of the brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f82fb087-c511-48b7-9e0b-9ec690a86ac7">SetColor</a>
</td>
<td align="left" width="63%">
Sets the color value and color profile of the brush.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMSolidColorBrush             *newInterface;
// The following values are defined outside of 
// this example.
//  XPS_COLOR                     color;
//  IXpsOMColorProfileResource    *colorProfile;

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
    hr = xpsFactory->CreateSolidColorBrush (
        &color,
        colorProfile,
        &newInterface);

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





## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/58690d93-9e3f-487c-956e-bb21122ecc96">IXpsOMObjectFactory::CreateSolidColorBrush</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

