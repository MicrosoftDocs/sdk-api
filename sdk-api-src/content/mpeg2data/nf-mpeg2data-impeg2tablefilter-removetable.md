---
UID: NF:mpeg2data.IMpeg2TableFilter.RemoveTable
title: IMpeg2TableFilter::RemoveTable (mpeg2data.h)
description: The RemoveTable method removes a table identifier (TID) from the list of MPEG-2 table sections that the filter sends.
helpviewer_keywords: ["IMpeg2TableFilter interface [Microsoft TV Technologies]","RemoveTable method","IMpeg2TableFilter.RemoveTable","IMpeg2TableFilter::RemoveTable","IMpeg2TableFilterRemoveTable","RemoveTable","RemoveTable method [Microsoft TV Technologies]","RemoveTable method [Microsoft TV Technologies]","IMpeg2TableFilter interface","mpeg2data/IMpeg2TableFilter::RemoveTable","mstv.impeg2tablefilter_removetable"]
old-location: mstv\impeg2tablefilter_removetable.htm
tech.root: mstv
ms.assetid: b8875340-48cf-47eb-a7cc-58e181df37fb
ms.date: 12/05/2018
ms.keywords: IMpeg2TableFilter interface [Microsoft TV Technologies],RemoveTable method, IMpeg2TableFilter.RemoveTable, IMpeg2TableFilter::RemoveTable, IMpeg2TableFilterRemoveTable, RemoveTable, RemoveTable method [Microsoft TV Technologies], RemoveTable method [Microsoft TV Technologies],IMpeg2TableFilter interface, mpeg2data/IMpeg2TableFilter::RemoveTable, mstv.impeg2tablefilter_removetable
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
 - IMpeg2TableFilter::RemoveTable
 - mpeg2data/IMpeg2TableFilter::RemoveTable
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
 - IMpeg2TableFilter.RemoveTable
---

# IMpeg2TableFilter::RemoveTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RemoveTable</b> method removes a table identifier (TID) from the list of MPEG-2 table sections that the filter sends.

## -parameters

### -param p [in]

Specifies the packet identifier (PID) of the table.

### -param t [in]

Specifies the TID to remove from the list.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2tablefilter">IMpeg2TableFilter Interface</a>