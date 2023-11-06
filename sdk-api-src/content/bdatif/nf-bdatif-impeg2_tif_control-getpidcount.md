---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.GetPIDCount
title: IMPEG2_TIF_CONTROL::GetPIDCount (bdatif.h)
description: The GetPIDCount method retrieves the number of MPEG-2 Packet IDs being filtered by the MPEG-2 Demultiplexer into the TIF's input data.
helpviewer_keywords: ["GetPIDCount","GetPIDCount method [Microsoft TV Technologies]","GetPIDCount method [Microsoft TV Technologies]","IMPEG2_TIF_CONTROL interface","IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","GetPIDCount method","IMPEG2_TIF_CONTROL.GetPIDCount","IMPEG2_TIF_CONTROL::GetPIDCount","IMPEG2_TIF_CONTROLGetPIDCount","bdatif/IMPEG2_TIF_CONTROL::GetPIDCount","mstv.impeg2_tif_control_getpidcount"]
old-location: mstv\impeg2_tif_control_getpidcount.htm
tech.root: mstv
ms.assetid: 2d77c3d8-b91c-43de-b4c1-bd41636eb4ad
ms.date: 12/05/2018
ms.keywords: GetPIDCount, GetPIDCount method [Microsoft TV Technologies], GetPIDCount method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],GetPIDCount method, IMPEG2_TIF_CONTROL.GetPIDCount, IMPEG2_TIF_CONTROL::GetPIDCount, IMPEG2_TIF_CONTROLGetPIDCount, bdatif/IMPEG2_TIF_CONTROL::GetPIDCount, mstv.impeg2_tif_control_getpidcount
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
 - IMPEG2_TIF_CONTROL::GetPIDCount
 - bdatif/IMPEG2_TIF_CONTROL::GetPIDCount
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
 - IMPEG2_TIF_CONTROL.GetPIDCount
---

# IMPEG2_TIF_CONTROL::GetPIDCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPIDCount</b> method retrieves the number of MPEG-2 Packet IDs being filtered by the <a href="/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> into the TIF's input data.

## -parameters

### -param pulcPIDs [out]

Pointer to a variable that receives the number of PIDs currently being filtered to the Demux.

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

A custom TIF extension might or might not need this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-impeg2_tif_control">IMPEG2_TIF_CONTROL Interface</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-getpids">IMPEG2_TIF_CONTROL::GetPIDs</a>