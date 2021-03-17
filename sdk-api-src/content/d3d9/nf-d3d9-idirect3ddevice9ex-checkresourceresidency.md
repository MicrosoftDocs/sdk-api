---
UID: NF:d3d9.IDirect3DDevice9Ex.CheckResourceResidency
title: IDirect3DDevice9Ex::CheckResourceResidency (d3d9.h)
description: Checks an array of resources to determine if it is likely that they will cause a large stall at Draw time because the system must make the resources GPU-accessible.
helpviewer_keywords: ["3b00074b-be34-94d5-7702-c5e8f870e68f","CheckResourceResidency","CheckResourceResidency method [Direct3D 9]","CheckResourceResidency method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","CheckResourceResidency method","IDirect3DDevice9Ex.CheckResourceResidency","IDirect3DDevice9Ex::CheckResourceResidency","d3d9/IDirect3DDevice9Ex::CheckResourceResidency","direct3d9.idirect3ddevice9ex_checkresourceresidency"]
old-location: direct3d9\idirect3ddevice9ex_checkresourceresidency.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_checkresourceresidency.htm
ms.date: 12/05/2018
ms.keywords: 3b00074b-be34-94d5-7702-c5e8f870e68f, CheckResourceResidency, CheckResourceResidency method [Direct3D 9], CheckResourceResidency method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CheckResourceResidency method, IDirect3DDevice9Ex.CheckResourceResidency, IDirect3DDevice9Ex::CheckResourceResidency, d3d9/IDirect3DDevice9Ex::CheckResourceResidency, direct3d9.idirect3ddevice9ex_checkresourceresidency
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9Ex::CheckResourceResidency
 - d3d9/IDirect3DDevice9Ex::CheckResourceResidency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9Ex.CheckResourceResidency
---

# IDirect3DDevice9Ex::CheckResourceResidency


## -description

Checks an array of resources to determine if it is likely that they will cause a large stall at Draw time because the system must make the resources GPU-accessible.

## -parameters

### -param pResourceArray [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>**</b>

An array of <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a> pointers that indicate the resources to check.

### -param NumResources [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT32</a></b>

A value indicating the number of resources passed into the <i>pResourceArray</i> parameter up to a maximum of 65535.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If all the resources are in GPU-accessible memory, the method will return S_OK. The system may need to perform a remapping operation to promote the resources, but will not have to copy data.

 If no allocation that comprises the resources is on disk, but at least one allocation is not in GPU-accessible memory, the method will return S_RESIDENT_IN_SHARED_MEMORY. The system may need to perform a copy to promote the resource.

 If at least one allocation that comprises the resources is on disk, this method will return S_NOT_RESIDENT.  The system may need to perform a copy to promote the resource.

## -remarks

This API is no more than a reasonable guess at residency, since resources may have been demoted by the time the application uses them.

The expected usage pattern is as follows. If the application determines that a set of resources are not resident, then the application will substitute a lower-LOD version of the resource and continue with rendering. The video memory manager API, offers a feature to allow the application to express that it would like these lower-LOD resources to be made more likely to stay resident in GPU-accessible memory. It is the app's responsibility to create, fill and destroy these lower-LOD versions, if it so chooses.

The application also needs to begin promotion of the higher-LOD versions when the residency check indicates that the resource is not resident in GPU-accessible memory. Since a per-process lock exists in kernel mode, a performant implementation will spawn a separate process whose sole job is to promote resources. The application communicates resource identity between the two process by means of the <a href="/windows/desktop/direct3d9/dx9lh">Sharing Resources</a> shared surfaces API and promotes them by means of the <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority">SetPriority</a>.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>