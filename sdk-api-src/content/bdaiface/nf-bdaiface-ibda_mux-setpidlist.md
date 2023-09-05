---
UID: NF:bdaiface.IBDA_MUX.SetPidList
title: IBDA_MUX::SetPidList (bdaiface.h)
description: Sets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.
helpviewer_keywords: ["IBDA_MUX interface [Microsoft TV Technologies]","SetPidList method","IBDA_MUX.SetPidList","IBDA_MUX::SetPidList","SetPidList","SetPidList method [Microsoft TV Technologies]","SetPidList method [Microsoft TV Technologies]","IBDA_MUX interface","bdaiface/IBDA_MUX::SetPidList","mstv.ibda_mux_setpidlist"]
old-location: mstv\ibda_mux_setpidlist.htm
tech.root: mstv
ms.assetid: 2d77086c-2321-434d-bf24-b4eac395825b
ms.date: 12/05/2018
ms.keywords: IBDA_MUX interface [Microsoft TV Technologies],SetPidList method, IBDA_MUX.SetPidList, IBDA_MUX::SetPidList, SetPidList, SetPidList method [Microsoft TV Technologies], SetPidList method [Microsoft TV Technologies],IBDA_MUX interface, bdaiface/IBDA_MUX::SetPidList, mstv.ibda_mux_setpidlist
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
 - IBDA_MUX::SetPidList
 - bdaiface/IBDA_MUX::SetPidList
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
 - IBDA_MUX.SetPidList
---

# IBDA_MUX::SetPidList


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.

## -parameters

### -param ulPidListCount [in]

The number of elements in the <i>pbPidListBuffer</i> array.

### -param pbPidListBuffer [in]

Pointer to an array of <a href="/previous-versions/windows/desktop/mstv/bda-mux-pidlistitem">BDA_MUX_PIDLISTITEM</a> structures.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_mux">IBDA_MUX</a>