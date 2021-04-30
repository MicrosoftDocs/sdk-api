---
UID: NF:d2d1_3.ID2D1ImageSource.TryReclaimResources
title: ID2D1ImageSource::TryReclaimResources (d2d1_3.h)
description: Restores access to resources that were previously offered by calling OfferResources.
helpviewer_keywords: ["ID2D1ImageSource interface [Direct2D]","TryReclaimResources method","ID2D1ImageSource.TryReclaimResources","ID2D1ImageSource::TryReclaimResources","TryReclaimResources","TryReclaimResources method [Direct2D]","TryReclaimResources method [Direct2D]","ID2D1ImageSource interface","d2d1_3/ID2D1ImageSource::TryReclaimResources","direct2d.id2d1imagesource_tryreclaimresources"]
old-location: direct2d\id2d1imagesource_tryreclaimresources.htm
tech.root: Direct2D
ms.assetid: 9639353D-EA3B-4ABD-A4DE-405B18218801
ms.date: 12/05/2018
ms.keywords: ID2D1ImageSource interface [Direct2D],TryReclaimResources method, ID2D1ImageSource.TryReclaimResources, ID2D1ImageSource::TryReclaimResources, TryReclaimResources, TryReclaimResources method [Direct2D], TryReclaimResources method [Direct2D],ID2D1ImageSource interface, d2d1_3/ID2D1ImageSource::TryReclaimResources, direct2d.id2d1imagesource_tryreclaimresources
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
req.lib: D2D1.lib
req.dll: D2D1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ImageSource::TryReclaimResources
 - d2d1_3/ID2D1ImageSource::TryReclaimResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.dll
api_name:
 - ID2D1ImageSource.TryReclaimResources
---

# ID2D1ImageSource::TryReclaimResources


## -description

Restores access to resources that were previously offered by calling <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1imagesource-offerresources">OfferResources</a>.

## -parameters

### -param resourcesDiscarded [out]

Type: <b>BOOL*</b>

Returns with TRUE if the corresponding resource’s content was discarded and is now undefined, or FALSE if the corresponding resource’s old content is still intact.
            The caller can pass in NULL, if the caller intends to fill the resources with new content regardless of whether the old content was discarded.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

<b>ReclaimResources</b> returns:

            

<ul>
<li><b>S_OK</b> if resources were successfully reclaimed
              </li>
<li><b>E_INVALIDARG</b> if the resources are invalid
              </li>
</ul>

## -remarks

After you call <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1imagesource-offerresources">OfferResources</a> to offer one or more resources, 
you must call <b>TryReclaimResources</b> before you can use those resources again. 
You must check the value in the <b>resourcesDiscarded</b> to determine whether the resource’s content was discarded. 
If a resource’s content was discarded while it was offered, its current content is undefined. Therefore, you must overwrite the resource’s content before you use the resource.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1imagesource">ID2D1ImageSource</a>