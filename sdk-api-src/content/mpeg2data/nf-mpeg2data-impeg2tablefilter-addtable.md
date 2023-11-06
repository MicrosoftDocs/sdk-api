---
UID: NF:mpeg2data.IMpeg2TableFilter.AddTable
title: IMpeg2TableFilter::AddTable (mpeg2data.h)
description: The AddTable method adds a table identifier (TID) to the list of MPEG-2 table sections that the filter sends.
helpviewer_keywords: ["AddTable","AddTable method [Microsoft TV Technologies]","AddTable method [Microsoft TV Technologies]","IMpeg2TableFilter interface","IMpeg2TableFilter interface [Microsoft TV Technologies]","AddTable method","IMpeg2TableFilter.AddTable","IMpeg2TableFilter::AddTable","IMpeg2TableFilterAddTable","mpeg2data/IMpeg2TableFilter::AddTable","mstv.impeg2tablefilter_addtable"]
old-location: mstv\impeg2tablefilter_addtable.htm
tech.root: mstv
ms.assetid: b789bfda-bb7e-4a7b-999e-0e2e798df4d5
ms.date: 12/05/2018
ms.keywords: AddTable, AddTable method [Microsoft TV Technologies], AddTable method [Microsoft TV Technologies],IMpeg2TableFilter interface, IMpeg2TableFilter interface [Microsoft TV Technologies],AddTable method, IMpeg2TableFilter.AddTable, IMpeg2TableFilter::AddTable, IMpeg2TableFilterAddTable, mpeg2data/IMpeg2TableFilter::AddTable, mstv.impeg2tablefilter_addtable
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
 - IMpeg2TableFilter::AddTable
 - mpeg2data/IMpeg2TableFilter::AddTable
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
 - IMpeg2TableFilter.AddTable
---

# IMpeg2TableFilter::AddTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>AddTable</b> method adds a table identifier (TID) to the list of MPEG-2 table sections that the filter sends.

## -parameters

### -param p [in]

Specifies the packet identifier (PID) of the transport stream packets to examine.

### -param t [in]

Specifies the TID of the section to retrieve.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2tablefilter">IMpeg2TableFilter Interface</a>