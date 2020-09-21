---
UID: NF:d3d11.ID3D11DeviceContext.Dispatch
title: ID3D11DeviceContext::Dispatch (d3d11.h)
description: Execute a command list from a thread group.
helpviewer_keywords: ["4643b8d4-3b6b-6d21-52bd-96e849a3eba7","Dispatch","Dispatch method [Direct3D 11]","Dispatch method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","Dispatch method","ID3D11DeviceContext.Dispatch","ID3D11DeviceContext::Dispatch","d3d11/ID3D11DeviceContext::Dispatch","direct3d11.id3d11devicecontext_dispatch"]
old-location: direct3d11\id3d11devicecontext_dispatch.htm
tech.root: direct3d11
ms.assetid: 7d3401bb-521f-4ab0-8833-e5caf712d0c9
ms.date: 12/05/2018
ms.keywords: 4643b8d4-3b6b-6d21-52bd-96e849a3eba7, Dispatch, Dispatch method [Direct3D 11], Dispatch method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],Dispatch method, ID3D11DeviceContext.Dispatch, ID3D11DeviceContext::Dispatch, d3d11/ID3D11DeviceContext::Dispatch, direct3d11.id3d11devicecontext_dispatch
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::Dispatch
 - d3d11/ID3D11DeviceContext::Dispatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.Dispatch
---

# ID3D11DeviceContext::Dispatch


## -description

Execute a command list from a thread group.

## -parameters

### -param ThreadGroupCountX [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of groups dispatched in the x direction. <i>ThreadGroupCountX</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).

### -param ThreadGroupCountY [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of groups dispatched in the y direction. <i>ThreadGroupCountY</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).

### -param ThreadGroupCountZ [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of groups dispatched in the z direction.  <i>ThreadGroupCountZ</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535). 
        In feature level 10 the value for <i>ThreadGroupCountZ</i> must be 1.

## -remarks

You call the <b>Dispatch</b> method to execute commands in a <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader">compute shader</a>. A compute shader can be run on many threads in parallel, within a thread group. Index a particular thread, within a thread group using a 3D vector 
      given by (x,y,z).

In the following illustration, assume a thread group with 50 threads where the size of the group is given by (5,5,2). A single thread is identified from a 
      thread group with 50 threads in it, using the vector (4,1,1).

<img alt="Illustration of a single thread within a thread group of 50 threads" src="./images/d3d11_thread_group_1.png"/>

The following illustration shows the relationship between the parameters passed to <b>ID3D11DeviceContext::Dispatch</b>, Dispatch(5,3,2), the values specified in the <a href="/windows/desktop/direct3dhlsl/sm5-attributes-numthreads">numthreads</a> attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values 
(<a href="/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)">SV_GroupIndex</a>,<a href="/windows/desktop/direct3dhlsl/sv-dispatchthreadid">SV_DispatchThreadID</a>,<a href="/windows/desktop/direct3dhlsl/sv-groupthreadid">SV_GroupThreadID</a>,<a href="/windows/desktop/direct3dhlsl/sv-groupid">SV_GroupID</a>).

<img alt="Illustration of the relationship between Dispatch, thread groups, and threads" src="./images/ThreadGroupIDs.png"/>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>