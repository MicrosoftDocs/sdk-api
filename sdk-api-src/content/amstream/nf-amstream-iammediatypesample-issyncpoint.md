---
UID: NF:amstream.IAMMediaTypeSample.IsSyncPoint
title: IAMMediaTypeSample::IsSyncPoint (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IsSyncPoint method determines if the beginning of a sample is a synchronization point.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","IsSyncPoint method","IAMMediaTypeSample.IsSyncPoint","IAMMediaTypeSample::IsSyncPoint","IAMMediaTypeSampleIsSyncPoint","IsSyncPoint","IsSyncPoint method [DirectShow]","IsSyncPoint method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::IsSyncPoint","dshow.iammediatypesample_issyncpoint"]
old-location: dshow\iammediatypesample_issyncpoint.htm
tech.root: dshow
ms.assetid: 0494f51e-2602-4574-88dd-0839a1d2f04f
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],IsSyncPoint method, IAMMediaTypeSample.IsSyncPoint, IAMMediaTypeSample::IsSyncPoint, IAMMediaTypeSampleIsSyncPoint, IsSyncPoint, IsSyncPoint method [DirectShow], IsSyncPoint method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::IsSyncPoint, dshow.iammediatypesample_issyncpoint
req.header: amstream.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaTypeSample::IsSyncPoint
 - amstream/IAMMediaTypeSample::IsSyncPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.IsSyncPoint
---

# IAMMediaTypeSample::IsSyncPoint


## -description

> [!NOTE]
>  This interface is deprecated. New applications should not use it.

The <code>IsSyncPoint</code> method determines if the beginning of a sample is a synchronization point.



## -returns

Returns S_OK if the beginning of the sample is a synchronization point, or S_FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
