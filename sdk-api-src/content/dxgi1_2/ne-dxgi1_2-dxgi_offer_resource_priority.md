---
UID: NE:dxgi1_2._DXGI_OFFER_RESOURCE_PRIORITY
title: DXGI_OFFER_RESOURCE_PRIORITY (dxgi1_2.h)
description: Identifies the importance of a resource’s content when you call the IDXGIDevice2::OfferResources method to offer the resource.
helpviewer_keywords: ["DXGI_OFFER_RESOURCE_PRIORITY","DXGI_OFFER_RESOURCE_PRIORITY enumeration [DXGI]","DXGI_OFFER_RESOURCE_PRIORITY_HIGH","DXGI_OFFER_RESOURCE_PRIORITY_LOW","DXGI_OFFER_RESOURCE_PRIORITY_NORMAL","direct3ddxgi._dxgi_offer_resource_priority","dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY","dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY_HIGH","dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY_LOW","dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY_NORMAL"]
old-location: direct3ddxgi\_dxgi_offer_resource_priority.htm
tech.root: direct3ddxgi
ms.assetid: BDC0AAA3-2B72-4732-82CE-458C14B0D993
ms.date: 12/05/2018
ms.keywords: DXGI_OFFER_RESOURCE_PRIORITY, DXGI_OFFER_RESOURCE_PRIORITY enumeration [DXGI], DXGI_OFFER_RESOURCE_PRIORITY_HIGH, DXGI_OFFER_RESOURCE_PRIORITY_LOW, DXGI_OFFER_RESOURCE_PRIORITY_NORMAL, direct3ddxgi._dxgi_offer_resource_priority, dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY, dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY_HIGH, dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY_LOW, dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY_NORMAL
req.header: dxgi1_2.h
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
targetos: Windows
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXGI_OFFER_RESOURCE_PRIORITY
 - dxgi1_2/_DXGI_OFFER_RESOURCE_PRIORITY
 - DXGI_OFFER_RESOURCE_PRIORITY
 - dxgi1_2/DXGI_OFFER_RESOURCE_PRIORITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_2.h
api_name:
 - DXGI_OFFER_RESOURCE_PRIORITY
---

# DXGI_OFFER_RESOURCE_PRIORITY enumeration


## -description

Identifies the importance of a resource’s content when you call the  <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a> method to offer the resource.

## -enum-fields

### -field DXGI_OFFER_RESOURCE_PRIORITY_LOW:1

The resource is low priority. The operating system discards a low priority resource before other offered resources with higher priority. It is a good programming practice to mark a resource as low priority if it has no useful content.

### -field DXGI_OFFER_RESOURCE_PRIORITY_NORMAL

The resource is normal priority. You mark a resource as normal priority if it has  content that is easy to regenerate.

### -field DXGI_OFFER_RESOURCE_PRIORITY_HIGH

The resource is high priority. The operating system discards other offered resources with lower priority before it discards a high priority resource.  You mark a resource as high priority if it has useful content that is difficult to regenerate.

## -remarks

Priority determines how likely the operating system is to discard an offered resource.  Resources offered with lower priority are discarded first.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources">IDXGIDevice2::ReclaimResource</a>
