---
UID: NF:bdaiface.IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes
title: IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes (bdaiface.h)
description: The get_SupportedDeviceNodeTypes method retrieves a list of the device node types that the demodulator supports.
helpviewer_keywords: ["IBDA_AutoDemodulateEx interface [Microsoft TV Technologies]","get_SupportedDeviceNodeTypes method","IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes","IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes","IBDA_AutoDemodulateExget_SupportedDeviceNodeTypes","bdaiface/IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes","get_SupportedDeviceNodeTypes","get_SupportedDeviceNodeTypes method [Microsoft TV Technologies]","get_SupportedDeviceNodeTypes method [Microsoft TV Technologies]","IBDA_AutoDemodulateEx interface","mstv.ibda_autodemodulateex_get_supporteddevicenodetypes"]
old-location: mstv\ibda_autodemodulateex_get_supporteddevicenodetypes.htm
tech.root: mstv
ms.assetid: 94d105f5-a609-4c10-b63e-61e39ee66fd3
ms.date: 12/05/2018
ms.keywords: IBDA_AutoDemodulateEx interface [Microsoft TV Technologies],get_SupportedDeviceNodeTypes method, IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes, IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes, IBDA_AutoDemodulateExget_SupportedDeviceNodeTypes, bdaiface/IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes, get_SupportedDeviceNodeTypes, get_SupportedDeviceNodeTypes method [Microsoft TV Technologies], get_SupportedDeviceNodeTypes method [Microsoft TV Technologies],IBDA_AutoDemodulateEx interface, mstv.ibda_autodemodulateex_get_supporteddevicenodetypes
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
 - IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes
 - bdaiface/IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes
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
 - IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes
---

# IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SupportedDeviceNodeTypes</b> method retrieves a list of the device node types that the demodulator supports.

## -parameters

### -param ulcDeviceNodeTypesMax [in]

Specifies the size of the <i>pguidDeviceNodeTypes</i> array.

### -param pulcDeviceNodeTypes [out]

If <i>pguidDeviceNodeTypes</i> is <b>NULL</b>, receives the number of device node types that the demodulator supports. If <i>pguidDeviceNodeTypes</i> is not <b>NULL</b>, receives the number of node types that were copied into the <i>pguidDeviceNodeTypes</i> array.

### -param pguidDeviceNodeTypes [in, out]

Pointer to an array of GUIDs, or <b>NULL</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If <i>pguidDeviceNodeTypes</i> is <b>NULL</b>, the method returns the number of supported node types in the <i>pulcDeviceNodeTypes</i> parameter. Otherwise, the method copies the node types into the <i>pguidDeviceNodeTypes</i> array, up to a maximum of <i>ulcDeviceNodeTypesMax</i>.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_autodemodulateex">IBDA_AutoDemodulateEx Interface</a>