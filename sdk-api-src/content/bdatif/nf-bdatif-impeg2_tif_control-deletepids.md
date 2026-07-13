---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.DeletePIDs
title: IMPEG2_TIF_CONTROL::DeletePIDs (bdatif.h)
description: The DeletePIDs method informs the Network Provider that the TIF no longer requires the specified PID.
helpviewer_keywords: ["DeletePIDs","DeletePIDs method [Microsoft TV Technologies]","DeletePIDs method [Microsoft TV Technologies]","IMPEG2_TIF_CONTROL interface","IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","DeletePIDs method","IMPEG2_TIF_CONTROL.DeletePIDs","IMPEG2_TIF_CONTROL::DeletePIDs","IMPEG2_TIF_CONTROLDeletePIDs","bdatif/IMPEG2_TIF_CONTROL::DeletePIDs","mstv.impeg2_tif_control_deletepids"]
old-location: mstv\impeg2_tif_control_deletepids.htm
tech.root: mstv
ms.assetid: d5188e30-6980-482f-a690-494855d6aeea
ms.date: 12/05/2018
ms.keywords: DeletePIDs, DeletePIDs method [Microsoft TV Technologies], DeletePIDs method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],DeletePIDs method, IMPEG2_TIF_CONTROL.DeletePIDs, IMPEG2_TIF_CONTROL::DeletePIDs, IMPEG2_TIF_CONTROLDeletePIDs, bdatif/IMPEG2_TIF_CONTROL::DeletePIDs, mstv.impeg2_tif_control_deletepids
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
 - IMPEG2_TIF_CONTROL::DeletePIDs
 - bdatif/IMPEG2_TIF_CONTROL::DeletePIDs
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
 - IMPEG2_TIF_CONTROL.DeletePIDs
---

# IMPEG2_TIF_CONTROL::DeletePIDs


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>DeletePIDs</b> method informs the Network Provider that the TIF no longer requires the specified PID.

## -parameters

### -param ulcPIDs [in]

Specifies the number of PIDs to delete. This value must equal the number of elements in the array specified by <i>pulPIDs</i>.

### -param pulPIDs [in]

Specifies an array of PID values containing <i>ulcPIDs</i> elements.

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

This method is called if a set of tables in the transport stream goes away, in order to remove the PSI/SI MPEG2 packet IDs from the TIF's data stream.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-impeg2_tif_control">IMPEG2_TIF_CONTROL Interface</a>