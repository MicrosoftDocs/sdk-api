---
UID: NN:bdaiface.IBDA_AutoDemodulateEx
title: IBDA_AutoDemodulateEx (bdaiface.h)
description: The IBDA_AutoDemodulateEx interface extends IBDA_AutoDemodulate.
helpviewer_keywords: ["IBDA_AutoDemodulateEx","IBDA_AutoDemodulateEx interface [Microsoft TV Technologies]","IBDA_AutoDemodulateEx interface [Microsoft TV Technologies]","described","IBDA_AutoDemodulateExInterface","bdaiface/IBDA_AutoDemodulateEx","mstv.ibda_autodemodulateex"]
old-location: mstv\ibda_autodemodulateex.htm
tech.root: mstv
ms.assetid: ecc642e4-7c36-400c-8a63-639f75b2bbc2
ms.date: 12/05/2018
ms.keywords: IBDA_AutoDemodulateEx, IBDA_AutoDemodulateEx interface [Microsoft TV Technologies], IBDA_AutoDemodulateEx interface [Microsoft TV Technologies],described, IBDA_AutoDemodulateExInterface, bdaiface/IBDA_AutoDemodulateEx, mstv.ibda_autodemodulateex
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
 - IBDA_AutoDemodulateEx
 - bdaiface/IBDA_AutoDemodulateEx
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
 - IBDA_AutoDemodulateEx
---

# IBDA_AutoDemodulateEx interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_AutoDemodulateEx</b> interface extends <a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_autodemodulate">IBDA_AutoDemodulate</a>. If a BDA device filter, specifically a demodulator, exposes this interface, it indicates that the filter can automatically detect signal characteristics. With this information, the Network Provider can be more efficient in managing the tuning process. For more information, see <b>KSPROPSETID_BdaAutodemodulate</b> in the Windows DDK.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

## -inheritance

The <b>IBDA_AutoDemodulateEx</b> interface inherits from <a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_autodemodulate">IBDA_AutoDemodulate</a>. <b>IBDA_AutoDemodulateEx</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_AutoDemodulateEx)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_autodemodulate">IBDA_AutoDemodulate</a>
