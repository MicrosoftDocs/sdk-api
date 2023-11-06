---
UID: NF:bdaiface.IBDA_FDC.RemoveTid
title: IBDA_FDC::RemoveTid (bdaiface.h)
description: Removes one or more table identifiers (TIDs) from the MPEG flow.
helpviewer_keywords: ["IBDA_FDC interface [Microsoft TV Technologies]","RemoveTid method","IBDA_FDC.RemoveTid","IBDA_FDC::RemoveTid","RemoveTid","RemoveTid method [Microsoft TV Technologies]","RemoveTid method [Microsoft TV Technologies]","IBDA_FDC interface","bdaiface/IBDA_FDC::RemoveTid","mstv.ibda_fdc_removetid"]
old-location: mstv\ibda_fdc_removetid.htm
tech.root: mstv
ms.assetid: fac8f486-e24e-4996-a90f-f8947d43d209
ms.date: 12/05/2018
ms.keywords: IBDA_FDC interface [Microsoft TV Technologies],RemoveTid method, IBDA_FDC.RemoveTid, IBDA_FDC::RemoveTid, RemoveTid, RemoveTid method [Microsoft TV Technologies], RemoveTid method [Microsoft TV Technologies],IBDA_FDC interface, bdaiface/IBDA_FDC::RemoveTid, mstv.ibda_fdc_removetid
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
 - IBDA_FDC::RemoveTid
 - bdaiface/IBDA_FDC::RemoveTid
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
 - IBDA_FDC.RemoveTid
---

# IBDA_FDC::RemoveTid


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Removes one or more table identifiers (TIDs) from the MPEG flow.

## -parameters

### -param TidsToRemove [in]

A comma-separated list of TIDs to remove.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_fdc">IBDA_FDC</a>