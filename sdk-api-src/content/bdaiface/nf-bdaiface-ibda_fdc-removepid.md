---
UID: NF:bdaiface.IBDA_FDC.RemovePid
title: IBDA_FDC::RemovePid (bdaiface.h)
description: Removes one or more packet identifiers (PIDs) from the MPEG flow.
helpviewer_keywords: ["IBDA_FDC interface [Microsoft TV Technologies]","RemovePid method","IBDA_FDC.RemovePid","IBDA_FDC::RemovePid","RemovePid","RemovePid method [Microsoft TV Technologies]","RemovePid method [Microsoft TV Technologies]","IBDA_FDC interface","bdaiface/IBDA_FDC::RemovePid","mstv.ibda_fdc_removepid"]
old-location: mstv\ibda_fdc_removepid.htm
tech.root: mstv
ms.assetid: 1277726c-6443-416c-a5d4-044d5f885af7
ms.date: 12/05/2018
ms.keywords: IBDA_FDC interface [Microsoft TV Technologies],RemovePid method, IBDA_FDC.RemovePid, IBDA_FDC::RemovePid, RemovePid, RemovePid method [Microsoft TV Technologies], RemovePid method [Microsoft TV Technologies],IBDA_FDC interface, bdaiface/IBDA_FDC::RemovePid, mstv.ibda_fdc_removepid
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
 - IBDA_FDC::RemovePid
 - bdaiface/IBDA_FDC::RemovePid
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
 - IBDA_FDC.RemovePid
---

# IBDA_FDC::RemovePid


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Removes one or more packet identifiers (PIDs) from the MPEG flow.

## -parameters

### -param PidsToRemove [in]

A comma-separated list of PIDs to remove.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 This command causes the device to send a delete_flow_req Application Protocol Data Unit (APDU).

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_fdc">IBDA_FDC</a>