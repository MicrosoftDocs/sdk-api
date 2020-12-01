---
UID: NF:amstream.IAMMediaTypeSample.SetMediaTime
title: IAMMediaTypeSample::SetMediaTime (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetMediaTime method sets the media time stamps for this sample.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetMediaTime method","IAMMediaTypeSample.SetMediaTime","IAMMediaTypeSample::SetMediaTime","IAMMediaTypeSampleSetMediaTime","SetMediaTime","SetMediaTime method [DirectShow]","SetMediaTime method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetMediaTime","dshow.iammediatypesample_setmediatime"]
old-location: dshow\iammediatypesample_setmediatime.htm
tech.root: dshow
ms.assetid: d255840f-9ff5-4eb0-b3b4-1295d77403f8
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetMediaTime method, IAMMediaTypeSample.SetMediaTime, IAMMediaTypeSample::SetMediaTime, IAMMediaTypeSampleSetMediaTime, SetMediaTime, SetMediaTime method [DirectShow], SetMediaTime method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetMediaTime, dshow.iammediatypesample_setmediatime
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
 - IAMMediaTypeSample::SetMediaTime
 - amstream/IAMMediaTypeSample::SetMediaTime
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
 - IAMMediaTypeSample.SetMediaTime
---

# IAMMediaTypeSample::SetMediaTime


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetMediaTime</code> method sets the media time stamps for this sample.

## -parameters

### -param pTimeStart [in]

Pointer to a variable that contains the media start time.

### -param pTimeEnd [in]

Pointer to a variable that contains the media stop time.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>