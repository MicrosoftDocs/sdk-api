---
UID: NF:d2d1_3.ID2D1ImageSource.OfferResources
title: ID2D1ImageSource::OfferResources
author: windows-sdk-content
description: Allows the operating system to free the video memory of resources by discarding their content.
old-location: direct2d\id2d1imagesource_offerresources.htm
tech.root: Direct2D
ms.assetid: 35728A9D-1D86-41EB-A760-B6B56D2576F3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ID2D1ImageSource interface [Direct2D],OfferResources method, ID2D1ImageSource.OfferResources, ID2D1ImageSource::OfferResources, OfferResources, OfferResources method [Direct2D], OfferResources method [Direct2D],ID2D1ImageSource interface, d2d1_3/ID2D1ImageSource::OfferResources, direct2d.id2d1imagesource_offerresources
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1ImageSource.OfferResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ImageSource::OfferResources


## -description


Allows the operating system to free the video memory of resources by discarding their content.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

<b>OfferResources</b> returns:
            

<ul>
<li><b>S_OK</b> if resources were successfully offered
              </li>
<li><b>E_INVALIDARG</b> if a resource in the array or the priority is invalid
              </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a9ee20db-98cf-bc5f-96d8-232073810cc5">ID2D1ImageSource</a>
 

 

