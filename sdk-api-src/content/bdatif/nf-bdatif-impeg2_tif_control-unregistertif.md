---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.UnregisterTIF
title: IMPEG2_TIF_CONTROL::UnregisterTIF (bdatif.h)
description: The UnregisterTIF method unregisters the TIF with the Network Provider.
helpviewer_keywords: ["IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","UnregisterTIF method","IMPEG2_TIF_CONTROL.UnregisterTIF","IMPEG2_TIF_CONTROL::UnregisterTIF","IMPEG2_TIF_CONTROLUnregisterTIF","UnregisterTIF","UnregisterTIF method [Microsoft TV Technologies]","UnregisterTIF method [Microsoft TV Technologies]","IMPEG2_TIF_CONTROL interface","bdatif/IMPEG2_TIF_CONTROL::UnregisterTIF","mstv.impeg2_tif_control_unregistertif"]
old-location: mstv\impeg2_tif_control_unregistertif.htm
tech.root: mstv
ms.assetid: e4fd151e-ec24-41b9-85df-fba05fc174d1
ms.date: 12/05/2018
ms.keywords: IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],UnregisterTIF method, IMPEG2_TIF_CONTROL.UnregisterTIF, IMPEG2_TIF_CONTROL::UnregisterTIF, IMPEG2_TIF_CONTROLUnregisterTIF, UnregisterTIF, UnregisterTIF method [Microsoft TV Technologies], UnregisterTIF method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, bdatif/IMPEG2_TIF_CONTROL::UnregisterTIF, mstv.impeg2_tif_control_unregistertif
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
 - IMPEG2_TIF_CONTROL::UnregisterTIF
 - bdatif/IMPEG2_TIF_CONTROL::UnregisterTIF
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
 - IMPEG2_TIF_CONTROL.UnregisterTIF
---

# IMPEG2_TIF_CONTROL::UnregisterTIF


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>UnregisterTIF</b> method unregisters the TIF with the Network Provider.

## -parameters

### -param pvRegistrationContext [in]

Identifier returned by the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-registertif">IMPEG2_TIF_CONTROL::RegisterTIF</a> method.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -remarks

Call this method after the TIF's input pin has been disconnected from the Demux.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-impeg2_tif_control">IMPEG2_TIF_CONTROL Interface</a>