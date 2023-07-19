---
UID: NF:bdaiface.IBDA_AutoDemodulateEx.get_AuxInputCount
title: IBDA_AutoDemodulateEx::get_AuxInputCount (bdaiface.h)
description: The get_AuxInputCount method retrieves a count of the number of auxiliary inputs on the demodulator.
helpviewer_keywords: ["IBDA_AutoDemodulateEx interface [Microsoft TV Technologies]","get_AuxInputCount method","IBDA_AutoDemodulateEx.get_AuxInputCount","IBDA_AutoDemodulateEx::get_AuxInputCount","IBDA_AutoDemodulateExget_AuxInputCount","bdaiface/IBDA_AutoDemodulateEx::get_AuxInputCount","get_AuxInputCount","get_AuxInputCount method [Microsoft TV Technologies]","get_AuxInputCount method [Microsoft TV Technologies]","IBDA_AutoDemodulateEx interface","mstv.ibda_autodemodulateex_get_auxinputcount"]
old-location: mstv\ibda_autodemodulateex_get_auxinputcount.htm
tech.root: mstv
ms.assetid: a23a1d54-377e-48cb-a4ff-dfd5a6972677
ms.date: 12/05/2018
ms.keywords: IBDA_AutoDemodulateEx interface [Microsoft TV Technologies],get_AuxInputCount method, IBDA_AutoDemodulateEx.get_AuxInputCount, IBDA_AutoDemodulateEx::get_AuxInputCount, IBDA_AutoDemodulateExget_AuxInputCount, bdaiface/IBDA_AutoDemodulateEx::get_AuxInputCount, get_AuxInputCount, get_AuxInputCount method [Microsoft TV Technologies], get_AuxInputCount method [Microsoft TV Technologies],IBDA_AutoDemodulateEx interface, mstv.ibda_autodemodulateex_get_auxinputcount
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - IBDA_AutoDemodulateEx::get_AuxInputCount
 - bdaiface/IBDA_AutoDemodulateEx::get_AuxInputCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_AutoDemodulateEx.get_AuxInputCount
---

# IBDA_AutoDemodulateEx::get_AuxInputCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AuxInputCount</b> method retrieves a count of the number of auxiliary inputs on the demodulator.

## -parameters

### -param pulCompositeCount [in, out]

Pointer to a variable that receives a count of the number of composite-video input connectors on the device.

### -param pulSvideoCount [in, out]

Pointer to a variable that receives a count of the number of S-Video input connectors on the device.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

<div class="alert"><b>Note</b>  The <i>pulCompositeCount</i> and <i>pulSvideoCount</i> parameters are marked in the IDL file as [in, out] but are used as [out] parameters. To preserve binary compatibility with previous versions, they have not been changed.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_autodemodulateex">IBDA_AutoDemodulateEx Interface</a>