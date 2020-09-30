---
UID: NF:amstream.IAMMediaTypeSample.SetSyncPoint
title: IAMMediaTypeSample::SetSyncPoint (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetSyncPoint method specifies whether the beginning of this sample is a synchronization point.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetSyncPoint method","IAMMediaTypeSample.SetSyncPoint","IAMMediaTypeSample::SetSyncPoint","IAMMediaTypeSampleSetSyncPoint","SetSyncPoint","SetSyncPoint method [DirectShow]","SetSyncPoint method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetSyncPoint","dshow.iammediatypesample_setsyncpoint"]
old-location: dshow\iammediatypesample_setsyncpoint.htm
tech.root: dshow
ms.assetid: d2ff9b33-c49c-4715-b580-f05670a0f405
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetSyncPoint method, IAMMediaTypeSample.SetSyncPoint, IAMMediaTypeSample::SetSyncPoint, IAMMediaTypeSampleSetSyncPoint, SetSyncPoint, SetSyncPoint method [DirectShow], SetSyncPoint method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetSyncPoint, dshow.iammediatypesample_setsyncpoint
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
 - IAMMediaTypeSample::SetSyncPoint
 - amstream/IAMMediaTypeSample::SetSyncPoint
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
 - IAMMediaTypeSample.SetSyncPoint
---

# IAMMediaTypeSample::SetSyncPoint


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetSyncPoint</code> method specifies whether the beginning of this sample is a synchronization point.

## -parameters

### -param bIsSyncPoint

Boolean value that specifies whether the beginning of this sample is a synchronization point. If <b>TRUE</b>, the beginning of the sample is a synchronization point.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>