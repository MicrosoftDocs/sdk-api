---
UID: NF:d2d1effectauthor.ID2D1EffectImpl.Initialize
title: ID2D1EffectImpl::Initialize
author: windows-sdk-content
description: The effect can use this method to do one time initialization tasks.
old-location: direct2d\id2d1effectimpl_initialize.htm
tech.root: direct2d
ms.assetid: BC5A6B97-6BA8-4C97-9F8B-D87EBCD80A98
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID2D1EffectImpl interface [Direct2D],Initialize method, ID2D1EffectImpl.Initialize, ID2D1EffectImpl::Initialize, Initialize, Initialize method [Direct2D], Initialize method [Direct2D],ID2D1EffectImpl interface, d2d1effectauthor/ID2D1EffectImpl::Initialize, direct2d.id2d1effectimpl_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectImpl.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectImpl::Initialize


## -description


The effect can use this method to do one time initialization tasks.  If this method is not needed, the method can just return <b>S_OK</b>.


## -parameters




### -param effectContext [in]

Type: <b><a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>*</b>

An internal context interface that creates and returns effect author–centric types.


### -param transformGraph [in]

Type: <b><a href="https://msdn.microsoft.com/6CA29200-9834-4A5B-99E8-434CD6E9B243">ID2D1TransformGraph</a>*</b>

The effect can
    populate the transform graph with a topology and can update it later.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This moves resource creation cost to the <a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">CreateEffect</a> call, rather than during rendering.

If the implementation fails this call, the corresponding <a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a> call also fails.

The following example shows an effect implementing an initialize method.


#### Examples

The example here shows an effect implementing an initialize method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>class CEffectImplementation : public ID2D1EffectImpl
{
public:

    virtual ~CEffectImplementation()
    {
        if (_pContextInternal != NULL)
        {
            _pContextInternal-&gt;Release();
        }
    }

    IFACEMETHODIMP Initialize(__in ID2D1DeviceContextInternal *pContextInternal, __in ID2D1TransformGraph *pTransformGraph)
    {
        HRESULT hr = S_OK;

        _pContextInternal = pContextInternal;
        _pContextInternal-&gt;AddRef();

								_pTransformGraph = pTransformGraph;
        _pTransformGraph&gt;AddRef();

								// Populate the transform graph.					    

        return S_OK;
    }

private:

    ID2D1EffectContext *_pContextInternal;
    ID2D1TransformGraph *_pTransformGraph;
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>
 

 

