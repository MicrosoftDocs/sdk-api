---
UID: NF:devicetopology.IAudioInputSelector.GetSelection
title: IAudioInputSelector::GetSelection (devicetopology.h)
description: The GetSelection method gets the local ID of the part that is connected to the selector input that is currently selected.
helpviewer_keywords: ["GetSelection","GetSelection method [Core Audio]","GetSelection method [Core Audio]","IAudioInputSelector interface","IAudioInputSelector interface [Core Audio]","GetSelection method","IAudioInputSelector.GetSelection","IAudioInputSelector::GetSelection","IAudioInputSelectorGetSelection","coreaudio.iaudioinputselector_getselection","devicetopology/IAudioInputSelector::GetSelection"]
old-location: coreaudio\iaudioinputselector_getselection.htm
tech.root: CoreAudio
ms.assetid: 38288a63-62a3-4b06-b2e6-dbe8c27e09ad
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Core Audio], GetSelection method [Core Audio],IAudioInputSelector interface, IAudioInputSelector interface [Core Audio],GetSelection method, IAudioInputSelector.GetSelection, IAudioInputSelector::GetSelection, IAudioInputSelectorGetSelection, coreaudio.iaudioinputselector_getselection, devicetopology/IAudioInputSelector::GetSelection
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IAudioInputSelector::GetSelection
 - devicetopology/IAudioInputSelector::GetSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioInputSelector.GetSelection
---

# IAudioInputSelector::GetSelection


## -description

The GetSelection method gets the local ID of the part that is connected to the selector input that is currently selected.

## -parameters

### -param pnIdSelected [out]

Pointer to a <b>UINT</b> variable into which the method writes the local ID of the part that directly links to the currently selected selector input.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pnIdSelected</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

A local ID is a number that uniquely identifies a part among all parts in a device topology. To obtain a pointer to the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface of a part from its local ID, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a> method.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioinputselector">IAudioInputSelector Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>