---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.RegisterTIF
title: IMPEG2_TIF_CONTROL::RegisterTIF (bdatif.h)
description: The RegisterTIF method is called by the Transport Information Filter (TIF) to register itself with the Network Provider.
helpviewer_keywords: ["IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","RegisterTIF method","IMPEG2_TIF_CONTROL.RegisterTIF","IMPEG2_TIF_CONTROL::RegisterTIF","IMPEG2_TIF_CONTROLRegisterTIF","RegisterTIF","RegisterTIF method [Microsoft TV Technologies]","RegisterTIF method [Microsoft TV Technologies]","IMPEG2_TIF_CONTROL interface","bdatif/IMPEG2_TIF_CONTROL::RegisterTIF","mstv.impeg2_tif_control_registertif"]
old-location: mstv\impeg2_tif_control_registertif.htm
tech.root: mstv
ms.assetid: d17b1f6b-24f4-40f4-9a58-aa582c0958f8
ms.date: 12/05/2018
ms.keywords: IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],RegisterTIF method, IMPEG2_TIF_CONTROL.RegisterTIF, IMPEG2_TIF_CONTROL::RegisterTIF, IMPEG2_TIF_CONTROLRegisterTIF, RegisterTIF, RegisterTIF method [Microsoft TV Technologies], RegisterTIF method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, bdatif/IMPEG2_TIF_CONTROL::RegisterTIF, mstv.impeg2_tif_control_registertif
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
 - IMPEG2_TIF_CONTROL::RegisterTIF
 - bdatif/IMPEG2_TIF_CONTROL::RegisterTIF
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
 - IMPEG2_TIF_CONTROL.RegisterTIF
---

# IMPEG2_TIF_CONTROL::RegisterTIF


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RegisterTIF</b> method is called by the Transport Information Filter (TIF) to register itself with the Network Provider.

## -parameters

### -param pUnkTIF [in]

Pointer to the TIF's <b>IUnknown</b> interface.

### -param ppvRegistrationContext [in, out]

Pointer to a variable that receives an identifier. Use this value as the parameter to the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-unregistertif">IMPEG2_TIF_CONTROL::UnregisterTIF</a> method.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Could not find a necessary interface on the TIF.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
A TIF is already registered with the Network Provider.

</td>
</tr>
</table>

## -remarks

Call this method immediately after the TIF's input pin is connected to the Demux.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-impeg2_tif_control">IMPEG2_TIF_CONTROL Interface</a>