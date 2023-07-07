---
UID: NF:tuner.ITunerCap.get_AuxInputCount
title: ITunerCap::get_AuxInputCount (tuner.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["ITunerCap interface [Microsoft TV Technologies]","get_AuxInputCount method","ITunerCap.get_AuxInputCount","ITunerCap::get_AuxInputCount","ITunerCapget_AuxInputCount","get_AuxInputCount","get_AuxInputCount method [Microsoft TV Technologies]","get_AuxInputCount method [Microsoft TV Technologies]","ITunerCap interface","mstv.itunercap_get_auxinputcount","tuner/ITunerCap::get_AuxInputCount"]
old-location: mstv\itunercap_get_auxinputcount.htm
tech.root: mstv
ms.assetid: a885d849-e6d8-477a-a629-1c1a6152bc9b
ms.date: 12/05/2018
ms.keywords: ITunerCap interface [Microsoft TV Technologies],get_AuxInputCount method, ITunerCap.get_AuxInputCount, ITunerCap::get_AuxInputCount, ITunerCapget_AuxInputCount, get_AuxInputCount, get_AuxInputCount method [Microsoft TV Technologies], get_AuxInputCount method [Microsoft TV Technologies],ITunerCap interface, mstv.itunercap_get_auxinputcount, tuner/ITunerCap::get_AuxInputCount
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - ITunerCap::get_AuxInputCount
 - tuner/ITunerCap::get_AuxInputCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITunerCap.get_AuxInputCount
---

# ITunerCap::get_AuxInputCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_AuxInputCount</b> method retrieves a count of the number of auxiliary inputs on the TV tuner.

## -parameters

### -param pulCompositeCount [in, out]

Receives a count of the number of composite-video input connectors on the device.

### -param pulSvideoCount [in, out]

Receives a count of the number of S-video input connectors on the device.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  The <i>pulCompositeCount</i> and <i>pulSvideoCount</i> parameters are marked in the IDL file as [in, out] but are used as [out] parameters. To preserve binary compatibility with previous versions, they have not been changed.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunercap">ITunerCap Interface</a>