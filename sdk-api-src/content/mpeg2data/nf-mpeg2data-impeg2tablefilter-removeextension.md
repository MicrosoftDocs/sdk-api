---
UID: NF:mpeg2data.IMpeg2TableFilter.RemoveExtension
title: IMpeg2TableFilter::RemoveExtension (mpeg2data.h)
description: The RemoveExtension method removes a table extension from the list of MPEG-2 table sections that the filter sends.
helpviewer_keywords: ["IMpeg2TableFilter interface [Microsoft TV Technologies]","RemoveExtension method","IMpeg2TableFilter.RemoveExtension","IMpeg2TableFilter::RemoveExtension","IMpeg2TableFilterRemoveExtension","RemoveExtension","RemoveExtension method [Microsoft TV Technologies]","RemoveExtension method [Microsoft TV Technologies]","IMpeg2TableFilter interface","mpeg2data/IMpeg2TableFilter::RemoveExtension","mstv.impeg2tablefilter_removeextension"]
old-location: mstv\impeg2tablefilter_removeextension.htm
tech.root: mstv
ms.assetid: 1f29f29d-d411-44b7-bedb-6d10c49a0d4d
ms.date: 12/05/2018
ms.keywords: IMpeg2TableFilter interface [Microsoft TV Technologies],RemoveExtension method, IMpeg2TableFilter.RemoveExtension, IMpeg2TableFilter::RemoveExtension, IMpeg2TableFilterRemoveExtension, RemoveExtension, RemoveExtension method [Microsoft TV Technologies], RemoveExtension method [Microsoft TV Technologies],IMpeg2TableFilter interface, mpeg2data/IMpeg2TableFilter::RemoveExtension, mstv.impeg2tablefilter_removeextension
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
 - IMpeg2TableFilter::RemoveExtension
 - mpeg2data/IMpeg2TableFilter::RemoveExtension
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
 - IMpeg2TableFilter.RemoveExtension
---

# IMpeg2TableFilter::RemoveExtension


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RemoveExtension</b> method removes a table extension from the list of MPEG-2 table sections that the filter sends.

## -parameters

### -param p [in]

Specifies the packet identifier (PID) of the table.

### -param t [in]

Specifies the table identifier (TID) of the table.

### -param e [in]

Specifies the table_extension identifier to remove from the list.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2tablefilter">IMpeg2TableFilter Interface</a>