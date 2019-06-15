---
UID: NN:d2d1effectauthor.ID2D1TransformGraph
title: ID2D1TransformGraph (d2d1effectauthor.h)
author: windows-sdk-content
description: Represents a graph of transform nodes.
old-location: direct2d\id2d1transformgraph.htm
tech.root: Direct2D
ms.assetid: 6CA29200-9834-4A5B-99E8-434CD6E9B243
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# ID2D1TransformGraph interface


## -description


Represents a graph of transform nodes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1TransformGraph</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1TransformGraph</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode">AddNode</a>
</td>
<td align="left" width="63%">
Adds the provided node to the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the transform nodes and all connections from the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode">ConnectNode</a>
</td>
<td align="left" width="63%">
Connects two nodes inside the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput">ConnectToEffectInput</a>
</td>
<td align="left" width="63%">
Connects a transform node inside the graph to the corresponding effect input of the encapsulating effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-getinputcount">GetInputCount</a>
</td>
<td align="left" width="63%">
Returns the number of inputs to the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-removenode">RemoveNode</a>
</td>
<td align="left" width="63%">
Removes the provided node from the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode">SetOutputNode</a>
</td>
<td align="left" width="63%">
Sets the output node for the transform graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setpassthroughgraph">SetPassthroughGraph</a>
</td>
<td align="left" width="63%">
Uses the specified input as the effect output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode">SetSingleTransformNode</a>
</td>
<td align="left" width="63%">
Sets a single transform node as being equivalent to the whole graph.

</td>
</tr>
</table> 


## -remarks



This interface allows a graph of transform nodes to be specified. This interface is passed to <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize">ID2D1EffectImpl::Initialize</a> to allow an effect implementation to specify a graph of transforms or a single transform.


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




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl">ID2D1EffectImpl</a>
 

 

