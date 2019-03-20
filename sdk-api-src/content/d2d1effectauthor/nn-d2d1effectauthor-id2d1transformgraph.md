---
UID: NN:d2d1effectauthor.ID2D1TransformGraph
title: ID2D1TransformGraph (d2d1effectauthor.h)
author: windows-sdk-content
description: Represents a graph of transform nodes.
old-location: direct2d\id2d1transformgraph.htm
tech.root: Direct2D
ms.assetid: 6CA29200-9834-4A5B-99E8-434CD6E9B243
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1TransformGraph, ID2D1TransformGraph interface [Direct2D], ID2D1TransformGraph interface [Direct2D],described, d2d1effectauthor/ID2D1TransformGraph, direct2d.id2d1transformgraph
ms.topic: interface
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1TransformGraph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TransformGraph interface


## -description


Represents a graph of transform nodes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1TransformGraph</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1TransformGraph</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1TransformGraph</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1937BD5F-C26A-4E67-8E07-688A24DA201E">AddNode</a>
</td>
<td align="left" width="63%">
Adds the provided node to the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7223A2FF-2B86-4080-B97E-BAE1C3E7000E">Clear</a>
</td>
<td align="left" width="63%">
Clears the transform nodes and all connections from the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59C7A366-804F-4CB3-A8CB-8617F226CE6B">ConnectNode</a>
</td>
<td align="left" width="63%">
Connects two nodes inside the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5190B887-4F3C-4304-A582-77585B438317">ConnectToEffectInput</a>
</td>
<td align="left" width="63%">
Connects a transform node inside the graph to the corresponding effect input of the encapsulating effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02CF2DE7-E1FD-4A6D-84FC-FA842EAE14C6">GetInputCount</a>
</td>
<td align="left" width="63%">
Returns the number of inputs to the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/075D43D7-0299-45E9-8C43-3EA37F0477CB">RemoveNode</a>
</td>
<td align="left" width="63%">
Removes the provided node from the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46C92F32-6D1B-49B8-B44A-F5415E670D9C">SetOutputNode</a>
</td>
<td align="left" width="63%">
Sets the output node for the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/719F7C82-31D7-40A0-BD5C-59F97F0002F9">SetPassthroughGraph</a>
</td>
<td align="left" width="63%">
Uses the specified input as the effect output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3E1B580C-88A5-4169-8E66-2BF9397C8DE9">SetSingleTransformNode</a>
</td>
<td align="left" width="63%">
Sets a single transform node as being equivalent to the whole graph.

</td>
</tr>
</table> 


## -remarks



This interface allows a graph of transform nodes to be specified. This interface is passed to <a href="https://msdn.microsoft.com/BC5A6B97-6BA8-4C97-9F8B-D87EBCD80A98">ID2D1EffectImpl::Initialize</a> to allow an effect implementation to specify a graph of transforms or a single transform.


#### Examples

This example shows how many of the methods on the <b>ID2D1TransformGraph</b> can be used.


```cpp

class CMyEffect : public ID2D1EffectImpl
{
public:

    IFACEMETHODIMP SetGraph(
       __in ID2D1TransformGraph *pGraph
       )
    {
        HRESULT hr = S_OK;

        hr = pGraph->Clear();

        if (SUCEEDED(hr))
        {
            hr = pGraph->AddNode(_pTransform1);
        }
   
        if (SUCCEEDED(hr))
        {
            hr = pGraph->AddNode(_pTransform2);
        }
 
        if (SUCCEEDED(hr))
        {
            hr = pGraph->SetOuputNode(_pTransform2);
        }

        if (SUCCEEDED(hr))
        {
            hr = pGraph->ConnectNode(_pTransform1, _pTransform2, 0);
        }

        if (SUCCEEDED(hr))
        {
            hr = pGraph->ConnectToEffectInput(0, _pTransform1, 0);
        }

        return hr;
    }

private:

    class CMyTransform1 : public ID2D1DrawTransform
    {
        // <Snip> The transform implementation, one node input</Snip>
    };

    class CMyTransform2 : public ID2D1DrawTransform
    {
 	   // <Snip> A second transform implementation one node input</Snip>
    };

    CMyTransform1 *_pTransform1;
    CMyTransform2 *_pTransform2;
};

```





## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>
 

 

