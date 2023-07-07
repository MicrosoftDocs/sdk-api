---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.GetPIDs
title: IMPEG2_TIF_CONTROL::GetPIDs (bdatif.h)
description: The GetPIDs method retrieves the list of MPEG-2 Packet IDs being filtered into the TIF's input data.
helpviewer_keywords: ["GetPIDs","GetPIDs method [Microsoft TV Technologies]","GetPIDs method [Microsoft TV Technologies]","IMPEG2_TIF_CONTROL interface","IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","GetPIDs method","IMPEG2_TIF_CONTROL.GetPIDs","IMPEG2_TIF_CONTROL::GetPIDs","IMPEG2_TIF_CONTROLGetPIDs","bdatif/IMPEG2_TIF_CONTROL::GetPIDs","mstv.impeg2_tif_control_getpids"]
old-location: mstv\impeg2_tif_control_getpids.htm
tech.root: mstv
ms.assetid: c7ca141b-e471-47ce-96b5-b2c0cad89daf
ms.date: 12/05/2018
ms.keywords: GetPIDs, GetPIDs method [Microsoft TV Technologies], GetPIDs method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],GetPIDs method, IMPEG2_TIF_CONTROL.GetPIDs, IMPEG2_TIF_CONTROL::GetPIDs, IMPEG2_TIF_CONTROLGetPIDs, bdatif/IMPEG2_TIF_CONTROL::GetPIDs, mstv.impeg2_tif_control_getpids
req.header: bdatif.h
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
 - IMPEG2_TIF_CONTROL::GetPIDs
 - bdatif/IMPEG2_TIF_CONTROL::GetPIDs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IMPEG2_TIF_CONTROL.GetPIDs
---

# IMPEG2_TIF_CONTROL::GetPIDs


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPIDs</b> method retrieves the list of MPEG-2 Packet IDs being filtered into the TIF's input data.

## -parameters

### -param pulcPIDs [out]

Pointer to a variable that receives the number of PIDs that were retrieved.

### -param pulPIDs [out]

Pointer to a variable that receives an array of returned <b>ULONG</b> values representing the PID values. The number of elements in the array is equal to the value of <i>pulcPIDs</i>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
</table>

## -remarks

A custom TIF extension might or might not have need for this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-impeg2_tif_control">IMPEG2_TIF_CONTROL Interface</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-addpids">IMPEG2_TIF_CONTROL::AddPIDs</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-getpidcount">IMPEG2_TIF_CONTROL::GetPIDCount</a>