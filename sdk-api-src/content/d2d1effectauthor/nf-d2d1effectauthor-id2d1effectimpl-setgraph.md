---
UID: NF:d2d1effectauthor.ID2D1EffectImpl.SetGraph
title: ID2D1EffectImpl::SetGraph
author: windows-sdk-content
description: The renderer calls this method to provide the effect implementation with a way to specify its transform graph and transform graph changes.
old-location: direct2d\id2d1effectimpl_setgraph.htm
tech.root: direct2d
ms.assetid: 3255CD0D-5B73-4020-965E-2CBBEF5BA35B
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1EffectImpl interface [Direct2D],SetGraph method, ID2D1EffectImpl.SetGraph, ID2D1EffectImpl::SetGraph, SetGraph, SetGraph method [Direct2D], SetGraph method [Direct2D],ID2D1EffectImpl interface, d2d1effectauthor/ID2D1EffectImpl::SetGraph, direct2d.id2d1effectimpl_setgraph
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
 - ID2D1EffectImpl.SetGraph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectImpl::SetGraph


## -description


The renderer calls this method to provide the effect implementation with a way to specify  its transform graph and transform graph changes. 

The renderer calls this method when:
<ul>
<li>When the effect is first initialized.</li>
<li>If the number of inputs to the effect changes.</li>
</ul>

## -parameters




### -param transformGraph

Type: <b><a href="https://msdn.microsoft.com/6CA29200-9834-4A5B-99E8-434CD6E9B243">ID2D1TransformGraph</a>*</b>

The graph to which the effect describes its transform topology through the SetDescription call.


## -returns



Type: <b>HRESULT</b>

An error that prevents the effect from being initialized if called as part of the CreateEffect call. If the effect fails a subsequent SetGraph call:

<ul>
<li>The error will be returned from the property method that caused the number of inputs to the effect to change.
</li>
<li>The effect object will be placed into an error state, if subsequently used to render, the context will be placed into a temporary error state, that particular effect will fail to render and the failure will be returned on the next EndDraw or Flush call.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>
 

 

