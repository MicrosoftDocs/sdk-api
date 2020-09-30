---
UID: NF:devicetopology.IAudioInputSelector.SetSelection
title: IAudioInputSelector::SetSelection (devicetopology.h)
description: The SetSelection method selects one of the inputs of the input selector.
helpviewer_keywords: ["IAudioInputSelector interface [Core Audio]","SetSelection method","IAudioInputSelector.SetSelection","IAudioInputSelector::SetSelection","IAudioInputSelectorSetSelection","SetSelection","SetSelection method [Core Audio]","SetSelection method [Core Audio]","IAudioInputSelector interface","coreaudio.iaudioinputselector_setselection","devicetopology/IAudioInputSelector::SetSelection"]
old-location: coreaudio\iaudioinputselector_setselection.htm
tech.root: CoreAudio
ms.assetid: b6291447-d3a9-4bc7-808c-9427e1642752
ms.date: 12/05/2018
ms.keywords: IAudioInputSelector interface [Core Audio],SetSelection method, IAudioInputSelector.SetSelection, IAudioInputSelector::SetSelection, IAudioInputSelectorSetSelection, SetSelection, SetSelection method [Core Audio], SetSelection method [Core Audio],IAudioInputSelector interface, coreaudio.iaudioinputselector_setselection, devicetopology/IAudioInputSelector::SetSelection
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
 - IAudioInputSelector::SetSelection
 - devicetopology/IAudioInputSelector::SetSelection
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
 - IAudioInputSelector.SetSelection
---

# IAudioInputSelector::SetSelection


## -description

The <b>SetSelection</b> method selects one of the inputs of the input selector.

## -parameters

### -param nIdSelect [in]

The new selector input. The caller should set this parameter to the local ID of a part that has a direct link to one of the selector inputs.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetSelection</b> call changes the state of the input-selector control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nIdSelect</i> is not the local ID of a part at a selector input.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

A local ID is a number that uniquely identifies a part among all parts in a device topology. To obtain the local ID of a part, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getlocalid">IPart::GetLocalId</a> method on the part object.

For a code example that calls the <b>SetSelection</b> method, see the implementation of the SelectCaptureDevice function in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioinputselector">IAudioInputSelector Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getlocalid">IPart::GetLocalId</a>