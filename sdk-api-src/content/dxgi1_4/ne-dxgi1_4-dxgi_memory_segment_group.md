---
UID: NE:dxgi1_4.DXGI_MEMORY_SEGMENT_GROUP
title: DXGI_MEMORY_SEGMENT_GROUP (dxgi1_4.h)
author: windows-sdk-content
description: Specifies the memory segment group to use.
old-location: direct3ddxgi\dxgi_memory_segment_group.htm
tech.root: direct3ddxgi
ms.assetid: 2FE35513-040E-41BF-866E-A13679C4F322
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXGI_MEMORY_SEGMENT_GROUP, DXGI_MEMORY_SEGMENT_GROUP enumeration [DXGI], DXGI_MEMORY_SEGMENT_GROUP_LOCAL, DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL, direct3ddxgi.dxgi_memory_segment_group, dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP, dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP_LOCAL, dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL
ms.topic: enum
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_4.h
api_name:
 - DXGI_MEMORY_SEGMENT_GROUP
product: Windows
targetos: Windows
req.typenames: DXGI_MEMORY_SEGMENT_GROUP
req.redist: 
ms.custom: 19H1
---

# DXGI_MEMORY_SEGMENT_GROUP enumeration


## -description


Specifies the memory segment group to use.


## -enum-fields




### -field DXGI_MEMORY_SEGMENT_GROUP_LOCAL

              The grouping of segments which is considered local to the video adapter, and represents the fastest available memory to the GPU. Applications should target the local segment group as the target size for their working set.


### -field DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL

The grouping of segments which is considered non-local to the video adapter, and may have slower performance than the local segment group.


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC">QueryVideoMemoryInfo</a> and <a href="https://msdn.microsoft.com/5D17F57F-9FFA-4B5C-98B6-33E5B3982A63">SetVideoMemoryReservation</a>.

Refer to the remarks for <a href="https://msdn.microsoft.com/EFA3FF00-F121-4ED8-AF83-1952C73AE06D">D3D12_MEMORY_POOL</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

