---
UID: NS:winnt._LUID
title: LUID (winnt.h)
description: Describes a local identifier for an adapter.
old-location: direct3ddxgi\_luid.htm
tech.root: direct3ddxgi
ms.assetid: 00601551-D6CE-4164-BDAF-DBCCF197990E
ms.date: 12/05/2018
ms.keywords: '*PLUID, LUID, LUID structure [DXGI], _LUID, direct3ddxgi._luid, winnt/LUID'
f1_keywords:
- winnt/LUID
dev_langs:
- c++
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- winnt.h
api_name:
- LUID
targetos: Windows
req.typenames: LUID, *PLUID
req.redist: 
ms.custom: 19H1
---

# LUID structure


## -description


Describes a local identifier for an adapter.


## -struct-fields




### -field LowPart

Specifies a DWORD that contains the unsigned lower numbers of the id.


### -field HighPart

Specifies a LONG that contains the signed high numbers of the id.


## -remarks



This structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getadapterluid">ID3D12Device::GetAdapterLuid</a> and <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid">GetSharedResourceAdapterLuid</a> methods.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>
 

 

