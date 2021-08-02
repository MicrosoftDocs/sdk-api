---
UID: NN:d2d1effectauthor.ID2D1TransformGraph
title: ID2D1TransformGraph (d2d1effectauthor.h)
description: Represents a graph of transform nodes.
helpviewer_keywords: ["ID2D1TransformGraph","ID2D1TransformGraph interface [Direct2D]","ID2D1TransformGraph interface [Direct2D]","described","d2d1effectauthor/ID2D1TransformGraph","direct2d.id2d1transformgraph"]
old-location: direct2d\id2d1transformgraph.htm
tech.root: Direct2D
ms.assetid: 6CA29200-9834-4A5B-99E8-434CD6E9B243
ms.date: 12/05/2018
ms.keywords: ID2D1TransformGraph, ID2D1TransformGraph interface [Direct2D], ID2D1TransformGraph interface [Direct2D],described, d2d1effectauthor/ID2D1TransformGraph, direct2d.id2d1transformgraph
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
 - ID2D1TransformGraph
 - d2d1effectauthor/ID2D1TransformGraph
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
 - ID2D1TransformGraph
---

# ID2D1TransformGraph interface


## -description

Represents a graph of transform nodes.

## -inheritance

The <b>ID2D1TransformGraph</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1TransformGraph</b> also has these types of members:

## -remarks

This interface allows a graph of transform nodes to be specified. This interface is passed to <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize">ID2D1EffectImpl::Initialize</a> to allow an effect implementation to specify a graph of transforms or a single transform.


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
            hr = pGraph->SetOutputNode(_pTransform2);
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

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl">ID2D1EffectImpl</a>
