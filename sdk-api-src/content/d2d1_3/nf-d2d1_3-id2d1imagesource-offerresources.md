---
UID: NF:d2d1_3.ID2D1ImageSource.OfferResources
title: ID2D1ImageSource::OfferResources (d2d1_3.h)
description: Allows the operating system to free the video memory of resources by discarding their content. (ID2D1ImageSource.OfferResources)
helpviewer_keywords: ["ID2D1ImageSource interface [Direct2D]","OfferResources method","ID2D1ImageSource.OfferResources","ID2D1ImageSource::OfferResources","OfferResources","OfferResources method [Direct2D]","OfferResources method [Direct2D]","ID2D1ImageSource interface","d2d1_3/ID2D1ImageSource::OfferResources","direct2d.id2d1imagesource_offerresources"]
old-location: direct2d\id2d1imagesource_offerresources.htm
tech.root: Direct2D
ms.assetid: 35728A9D-1D86-41EB-A760-B6B56D2576F3
ms.date: 12/05/2018
ms.keywords: ID2D1ImageSource interface [Direct2D],OfferResources method, ID2D1ImageSource.OfferResources, ID2D1ImageSource::OfferResources, OfferResources, OfferResources method [Direct2D], OfferResources method [Direct2D],ID2D1ImageSource interface, d2d1_3/ID2D1ImageSource::OfferResources, direct2d.id2d1imagesource_offerresources
req.header: d2d1_3.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ImageSource::OfferResources
 - d2d1_3/ID2D1ImageSource::OfferResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1ImageSource.OfferResources
---

# ID2D1ImageSource::OfferResources


## -description

Allows the operating system to free the video memory of resources by discarding their content.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

<b>OfferResources</b> returns:
            

<ul>
<li><b>S_OK</b> if resources were successfully offered
              </li>
<li><b>E_INVALIDARG</b> if a resource in the array or the priority is invalid
              </li>
</ul>

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1imagesource">ID2D1ImageSource</a>
