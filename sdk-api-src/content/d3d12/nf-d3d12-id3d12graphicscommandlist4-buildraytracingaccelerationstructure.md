---
UID: NF:d3d12.ID3D12GraphicsCommandList4.BuildRaytracingAccelerationStructure
title: ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure
author: windows-sdk-content
description: Performs a raytracing acceleration structure build on the GPU and optionally outputs post-build information immediately after the build.
old-location: direct3d12\id3d12graphicscommandlist4_buildraytracingaccelerationstructure.htm
tech.root: direct3d12
ms.assetid: B714530C-40E6-4C67-8908-373BB26E6635
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: BuildRaytracingAccelerationStructure, BuildRaytracingAccelerationStructure method, BuildRaytracingAccelerationStructure method,ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,BuildRaytracingAccelerationStructure method, ID3D12GraphicsCommandList4.BuildRaytracingAccelerationStructure, ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure, d3d12/ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure, direct3d12.id3d12graphicscommandlist4_buildraytracingaccelerationstructure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12GraphicsCommandList4.BuildRaytracingAccelerationStructure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Performs a raytracing acceleration structure build on the GPU and optionally outputs post-build information immediately after the build.  


## -parameters




### -param pDesc [in]

Description of the acceleration structure to build.


### -param NumPostbuildInfoDescs [in]

Size of the <i>pPostbuildInfoDescs</i> array.  Set to 0 if no post-build info is needed.


### -param pPostbuildInfoDescs [in]

Optional array of descriptions for post-build info to generate describing properties of the acceleration structure that was built.


## -returns



This method does not return a value.




## -remarks



This method can be called on graphics or compute command lists but not from bundles.

Post-build information can also be obtained separately from an already built acceleration structure by calling <a href="http://docs.microsoft.com/windows/desktop/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a>.  The advantage of generating post-build info along with a build is that a barrier isn’t needed in between the build completing and requesting post-build information, enabling scenarios where the app needs the post-build info right away.




## -see-also




<a href="direct3d12.id3d12graphicscommandlist4">ID3D12GraphicsCommandList4</a>
 

 

