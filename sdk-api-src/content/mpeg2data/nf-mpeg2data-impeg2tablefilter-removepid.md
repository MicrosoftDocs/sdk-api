---
UID: NF:mpeg2data.IMpeg2TableFilter.RemovePID
title: IMpeg2TableFilter::RemovePID (mpeg2data.h)
description: The RemovePID method removes a packet identifier (PID) from the list of PIDs that the filter sends.
helpviewer_keywords: ["IMpeg2TableFilter interface [Microsoft TV Technologies]","RemovePID method","IMpeg2TableFilter.RemovePID","IMpeg2TableFilter::RemovePID","IMpeg2TableFilterRemovePID","RemovePID","RemovePID method [Microsoft TV Technologies]","RemovePID method [Microsoft TV Technologies]","IMpeg2TableFilter interface","mpeg2data/IMpeg2TableFilter::RemovePID","mstv.impeg2tablefilter_removepid"]
old-location: mstv\impeg2tablefilter_removepid.htm
tech.root: mstv
ms.assetid: e9ce49e3-e256-4150-ab73-b57ed34ab30c
ms.date: 12/05/2018
ms.keywords: IMpeg2TableFilter interface [Microsoft TV Technologies],RemovePID method, IMpeg2TableFilter.RemovePID, IMpeg2TableFilter::RemovePID, IMpeg2TableFilterRemovePID, RemovePID, RemovePID method [Microsoft TV Technologies], RemovePID method [Microsoft TV Technologies],IMpeg2TableFilter interface, mpeg2data/IMpeg2TableFilter::RemovePID, mstv.impeg2tablefilter_removepid
req.header: mpeg2data.h
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
 - IMpeg2TableFilter::RemovePID
 - mpeg2data/IMpeg2TableFilter::RemovePID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2TableFilter.RemovePID
---

# IMpeg2TableFilter::RemovePID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RemovePID</b> method removes a packet identifier (PID) from the list of PIDs that the filter sends.

## -parameters

### -param p [in]

Specifies the PID to remove from the list.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2tablefilter">IMpeg2TableFilter Interface</a>