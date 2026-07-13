---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.AddPIDs
title: IMPEG2_TIF_CONTROL::AddPIDs (bdatif.h)
description: The AddPIDs method tells the Network Provider which PIDs the TIF should receive.
helpviewer_keywords: ["AddPIDs","AddPIDs method [Microsoft TV Technologies]","AddPIDs method [Microsoft TV Technologies]","IMPEG2_TIF_CONTROL interface","IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","AddPIDs method","IMPEG2_TIF_CONTROL.AddPIDs","IMPEG2_TIF_CONTROL::AddPIDs","IMPEG2_TIF_CONTROLAddPIDs","bdatif/IMPEG2_TIF_CONTROL::AddPIDs","mstv.impeg2_tif_control_addpids"]
old-location: mstv\impeg2_tif_control_addpids.htm
tech.root: mstv
ms.assetid: 27add7cc-1d77-4ac5-b63f-757f63f4c9b8
ms.date: 12/05/2018
ms.keywords: AddPIDs, AddPIDs method [Microsoft TV Technologies], AddPIDs method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],AddPIDs method, IMPEG2_TIF_CONTROL.AddPIDs, IMPEG2_TIF_CONTROL::AddPIDs, IMPEG2_TIF_CONTROLAddPIDs, bdatif/IMPEG2_TIF_CONTROL::AddPIDs, mstv.impeg2_tif_control_addpids
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
 - IMPEG2_TIF_CONTROL::AddPIDs
 - bdatif/IMPEG2_TIF_CONTROL::AddPIDs
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
 - IMPEG2_TIF_CONTROL.AddPIDs
---

# IMPEG2_TIF_CONTROL::AddPIDs


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>AddPIDs</b> method tells the Network Provider which PIDs the TIF should receive.

## -parameters

### -param ulcPIDs [in]

Specifies the number of PIDs to add. This value must be equal to the number of elements in the array specified by <i>pulPIDs</i>.

### -param pulPIDs [in]

Specifies an array of PID values to add. The array must contain <i>ulcPIDs</i> elements.

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

Only the TIF knows which table sections it requires. It uses this method to tell the Network Provider the PIDs for the packets that contain those tables. The Network Provider forwards the information to the Demux, which immediately begins routing packets with the specified PIDs to the TIF.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-impeg2_tif_control">IMPEG2_TIF_CONTROL Interface</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-getpids">IMPEG2_TIF_CONTROL::GetPIDs</a>