---
UID: NF:bdaiface.IBDA_FDC.AddTid
title: IBDA_FDC::AddTid (bdaiface.h)
description: Adds one or more table identifiers (TIDs) to the MPEG flow.
helpviewer_keywords: ["AddTid","AddTid method [Microsoft TV Technologies]","AddTid method [Microsoft TV Technologies]","IBDA_FDC interface","IBDA_FDC interface [Microsoft TV Technologies]","AddTid method","IBDA_FDC.AddTid","IBDA_FDC::AddTid","bdaiface/IBDA_FDC::AddTid","mstv.ibda_fdc_addtid"]
old-location: mstv\ibda_fdc_addtid.htm
tech.root: mstv
ms.assetid: 2cd39bbc-106b-4411-bc42-a1adc360e121
ms.date: 12/05/2018
ms.keywords: AddTid, AddTid method [Microsoft TV Technologies], AddTid method [Microsoft TV Technologies],IBDA_FDC interface, IBDA_FDC interface [Microsoft TV Technologies],AddTid method, IBDA_FDC.AddTid, IBDA_FDC::AddTid, bdaiface/IBDA_FDC::AddTid, mstv.ibda_fdc_addtid
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
 - IBDA_FDC::AddTid
 - bdaiface/IBDA_FDC::AddTid
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
 - IBDA_FDC.AddTid
---

# IBDA_FDC::AddTid


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Adds one or more table identifiers (TIDs) to the MPEG flow.

## -parameters

### -param TidsToAdd [in]

A comma-separated list of TIDs.

### -param CurrentTidList [out]

Receives a comma-separated list of the current TIDs. The caller must release the string by calling <b>SysFreeString</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_fdc">IBDA_FDC</a>