---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.SetSingleTransformNode
title: ID2D1TransformGraph::SetSingleTransformNode (d2d1effectauthor.h)
description: Sets a single transform node as being equivalent to the whole graph.
helpviewer_keywords: ["ID2D1TransformGraph interface [Direct2D]","SetSingleTransformNode method","ID2D1TransformGraph.SetSingleTransformNode","ID2D1TransformGraph::SetSingleTransformNode","SetSingleTransformNode","SetSingleTransformNode method [Direct2D]","SetSingleTransformNode method [Direct2D]","ID2D1TransformGraph interface","d2d1effectauthor/ID2D1TransformGraph::SetSingleTransformNode","direct2d.id2d1transformgraph_setsingletransformnode"]
old-location: direct2d\id2d1transformgraph_setsingletransformnode.htm
tech.root: Direct2D
ms.assetid: 3E1B580C-88A5-4169-8E66-2BF9397C8DE9
ms.date: 12/05/2018
ms.keywords: ID2D1TransformGraph interface [Direct2D],SetSingleTransformNode method, ID2D1TransformGraph.SetSingleTransformNode, ID2D1TransformGraph::SetSingleTransformNode, SetSingleTransformNode, SetSingleTransformNode method [Direct2D], SetSingleTransformNode method [Direct2D],ID2D1TransformGraph interface, d2d1effectauthor/ID2D1TransformGraph::SetSingleTransformNode, direct2d.id2d1transformgraph_setsingletransformnode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1TransformGraph::SetSingleTransformNode
 - d2d1effectauthor/ID2D1TransformGraph::SetSingleTransformNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1TransformGraph.SetSingleTransformNode
---

# ID2D1TransformGraph::SetSingleTransformNode


## -description

Sets a single transform node as being equivalent to the whole graph.

## -parameters

### -param node

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>*</b>

The node to be set.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
</table>

## -remarks

This equivalent to calling <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-clear">ID2D1TransformGraph::Clear</a>, adding a single node, connecting all of the node inputs to the effect inputs in order, and setting the transform not as the graph output.


#### Examples


```cpp
class CMySimpleEffect : public ID2D1EffectImpl
{
public:

    IFACEMETHODIMP SetGraph(
        __in ID2D1TransformGraph   *pGraph
        )
    {
        HRESULT hr = S_OK;

        CMyTransform *pTransform = new CMyTransform();
  
        hr = pTransform ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            hr = graph->SetSingleTransformNode(pTransform);

            pTransform->Release();
        }

        return hr;
    }

private:

    class CMyTransform : public ID2D1DrawTransform
    {
        // <Snip> Implementation of transform </Snip> 
    };

    
};

```

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph">ID2D1TransformGraph</a>