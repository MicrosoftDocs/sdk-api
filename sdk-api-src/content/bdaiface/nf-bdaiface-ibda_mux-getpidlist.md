---
UID: NF:bdaiface.IBDA_MUX.GetPidList
title: IBDA_MUX::GetPidList (bdaiface.h)
description: Gets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.
helpviewer_keywords: ["GetPidList","GetPidList method [Microsoft TV Technologies]","GetPidList method [Microsoft TV Technologies]","IBDA_MUX interface","IBDA_MUX interface [Microsoft TV Technologies]","GetPidList method","IBDA_MUX.GetPidList","IBDA_MUX::GetPidList","bdaiface/IBDA_MUX::GetPidList","mstv.ibda_mux_getpidlist"]
old-location: mstv\ibda_mux_getpidlist.htm
tech.root: mstv
ms.assetid: 92b13d40-4841-45ce-b232-5e29a93d71c5
ms.date: 12/05/2018
ms.keywords: GetPidList, GetPidList method [Microsoft TV Technologies], GetPidList method [Microsoft TV Technologies],IBDA_MUX interface, IBDA_MUX interface [Microsoft TV Technologies],GetPidList method, IBDA_MUX.GetPidList, IBDA_MUX::GetPidList, bdaiface/IBDA_MUX::GetPidList, mstv.ibda_mux_getpidlist
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows�7 [desktop apps only]
req.target-min-winversvr: Windows Server�2008�R2 [desktop apps only]
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
 - IBDA_MUX::GetPidList
 - bdaiface/IBDA_MUX::GetPidList
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
 - IBDA_MUX.GetPidList
---

# IBDA_MUX::GetPidList


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.

## -parameters

### -param pulPidListCount [in, out]

On input, specifies the size, in array elements, of the <i>pbPidListBuffer</i> array. On output, receives the number of PIDs.

### -param pbPidListBuffer [in, out]

Pointer to an array of <a href="/previous-versions/windows/desktop/mstv/bda-mux-pidlistitem">BDA_MUX_PIDLISTITEM</a> structures. The method fills in the array with the list of PIDs.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_SUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbPidListBuffer</i> array is too small.

</td>
</tr>
</table>

## -remarks

If the <i>pbPidListBuffer</i> array is too small, the method returns <b>E_NOT_SUFFICIENT_BUFFER</b> and sets the required size in the <i>pulPidListCount</i> parameter.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_mux">IBDA_MUX</a>