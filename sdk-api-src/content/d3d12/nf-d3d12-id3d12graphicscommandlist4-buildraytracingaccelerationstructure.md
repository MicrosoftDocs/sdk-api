---
UID: NF:d3d12.ID3D12GraphicsCommandList4.BuildRaytracingAccelerationStructure
title: ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure (d3d12.h)
description: Performs a raytracing acceleration structure build on the GPU and optionally outputs post-build information immediately after the build.
helpviewer_keywords: ["BuildRaytracingAccelerationStructure","BuildRaytracingAccelerationStructure method","BuildRaytracingAccelerationStructure method","ID3D12GraphicsCommandList4 interface","ID3D12GraphicsCommandList4 interface","BuildRaytracingAccelerationStructure method","ID3D12GraphicsCommandList4.BuildRaytracingAccelerationStructure","ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure","d3d12/ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure","direct3d12.id3d12graphicscommandlist4_buildraytracingaccelerationstructure"]
old-location: direct3d12\id3d12graphicscommandlist4_buildraytracingaccelerationstructure.htm
tech.root: direct3d12
ms.assetid: B714530C-40E6-4C67-8908-373BB26E6635
ms.date: 12/05/2018
ms.keywords: BuildRaytracingAccelerationStructure, BuildRaytracingAccelerationStructure method, BuildRaytracingAccelerationStructure method,ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,BuildRaytracingAccelerationStructure method, ID3D12GraphicsCommandList4.BuildRaytracingAccelerationStructure, ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure, d3d12/ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure, direct3d12.id3d12graphicscommandlist4_buildraytracingaccelerationstructure
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure
 - d3d12/ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12GraphicsCommandList4.BuildRaytracingAccelerationStructure
---

# ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure


## -description

Performs a raytracing acceleration structure build on the GPU and optionally outputs post-build information immediately after the build.

## -parameters

### -param pDesc [in]

Description of the acceleration structure to build.

### -param NumPostbuildInfoDescs [in]

Size of the <i>pPostbuildInfoDescs</i> array.  Set to 0 if no post-build info is needed.

### -param pPostbuildInfoDescs [in]

Optional array of descriptions for post-build info to generate describing properties of the acceleration structure that was built.

## -remarks

This method can be called on graphics or compute command lists but not from bundles.

Post-build information can also be obtained separately from an already built acceleration structure by calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a>.  The advantage of generating post-build info along with a build is that a barrier isn’t needed in between the build completing and requesting post-build information, enabling scenarios where the app needs the post-build info right away.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12graphicscommandlist4.md">ID3D12GraphicsCommandList4</a>
