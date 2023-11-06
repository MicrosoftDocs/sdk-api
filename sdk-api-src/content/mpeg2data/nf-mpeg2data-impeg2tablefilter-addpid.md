---
UID: NF:mpeg2data.IMpeg2TableFilter.AddPID
title: IMpeg2TableFilter::AddPID (mpeg2data.h)
description: The AddPID method adds a packet identifier (PID) to the list of PIDs that the filter sends.
helpviewer_keywords: ["AddPID","AddPID method [Microsoft TV Technologies]","AddPID method [Microsoft TV Technologies]","IMpeg2TableFilter interface","IMpeg2TableFilter interface [Microsoft TV Technologies]","AddPID method","IMpeg2TableFilter.AddPID","IMpeg2TableFilter::AddPID","IMpeg2TableFilterAddPID","mpeg2data/IMpeg2TableFilter::AddPID","mstv.impeg2tablefilter_addpid"]
old-location: mstv\impeg2tablefilter_addpid.htm
tech.root: mstv
ms.assetid: 7a811d1f-cb1b-4f45-8dee-ba83efd20709
ms.date: 12/05/2018
ms.keywords: AddPID, AddPID method [Microsoft TV Technologies], AddPID method [Microsoft TV Technologies],IMpeg2TableFilter interface, IMpeg2TableFilter interface [Microsoft TV Technologies],AddPID method, IMpeg2TableFilter.AddPID, IMpeg2TableFilter::AddPID, IMpeg2TableFilterAddPID, mpeg2data/IMpeg2TableFilter::AddPID, mstv.impeg2tablefilter_addpid
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
 - IMpeg2TableFilter::AddPID
 - mpeg2data/IMpeg2TableFilter::AddPID
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
 - IMpeg2TableFilter.AddPID
---

# IMpeg2TableFilter::AddPID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>AddPID</b> method adds a packet identifier (PID) to the list of PIDs that the filter sends.

## -parameters

### -param p [in]

Specifies the PID of the transport stream packets to examine.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2tablefilter">IMpeg2TableFilter Interface</a>