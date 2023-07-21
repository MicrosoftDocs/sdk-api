---
UID: NF:bdaiface.IBDA_FDC.RequestTables
title: IBDA_FDC::RequestTables (bdaiface.h)
description: Requests MPEG-2 table sections, filtered by table identifier (TID).
helpviewer_keywords: ["IBDA_FDC interface [Microsoft TV Technologies]","RequestTables method","IBDA_FDC.RequestTables","IBDA_FDC::RequestTables","RequestTables","RequestTables method [Microsoft TV Technologies]","RequestTables method [Microsoft TV Technologies]","IBDA_FDC interface","bdaiface/IBDA_FDC::RequestTables","mstv.ibda_fdc_requesttables"]
old-location: mstv\ibda_fdc_requesttables.htm
tech.root: mstv
ms.assetid: ff8483d3-6c4c-4786-a99b-bf3575a18fdb
ms.date: 12/05/2018
ms.keywords: IBDA_FDC interface [Microsoft TV Technologies],RequestTables method, IBDA_FDC.RequestTables, IBDA_FDC::RequestTables, RequestTables, RequestTables method [Microsoft TV Technologies], RequestTables method [Microsoft TV Technologies],IBDA_FDC interface, bdaiface/IBDA_FDC::RequestTables, mstv.ibda_fdc_requesttables
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_FDC::RequestTables
 - bdaiface/IBDA_FDC::RequestTables
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_FDC.RequestTables
---

# IBDA_FDC::RequestTables


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Requests MPEG-2 table sections, filtered by table identifier (TID).

## -parameters

### -param TableIDs [in]

A comma-separated list of TIDs.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_fdc">IBDA_FDC</a>