---
UID: NF:devicetopology.IPart.Activate
title: IPart::Activate (devicetopology.h)
description: The Activate method activates a function-specific interface on a connector or subunit.
helpviewer_keywords: ["Activate","Activate method [Core Audio]","Activate method [Core Audio]","IPart interface","IPart interface [Core Audio]","Activate method","IPart.Activate","IPart::Activate","IPartActivate","coreaudio.ipart_activate","devicetopology/IPart::Activate"]
old-location: coreaudio\ipart_activate.htm
tech.root: CoreAudio
ms.assetid: 72e08a30-65c0-437b-9932-110ba48a2376
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Core Audio], Activate method [Core Audio],IPart interface, IPart interface [Core Audio],Activate method, IPart.Activate, IPart::Activate, IPartActivate, coreaudio.ipart_activate, devicetopology/IPart::Activate
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
 - IPart::Activate
 - devicetopology/IPart::Activate
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
 - IPart.Activate
---

# IPart::Activate


## -description

The <b>Activate</b> method activates a function-specific interface on a connector or subunit.

## -parameters

### -param dwClsContext [in]

The execution context in which the code that manages the newly created object will run. The caller can restrict the context by setting this parameter to the bitwise <b>OR</b> of one or more <b>CLSCTX</b> enumeration values. The client can avoid imposing any context restrictions by specifying CLSCTX_ALL. For more information about <b>CLSCTX</b>, see the Windows SDK documentation.

### -param refiid [in]

The interface ID for the requested control function. The client should set this parameter to one of the following <b>REFIID</b> values:

IID_IAudioAutoGainControl

IID_IAudioBass

IID_IAudioChannelConfig

IID_IAudioInputSelector

IID_IAudioLoudness

IID_IAudioMidrange

IID_IAudioMute

IID_IAudioOutputSelector

IID_IAudioPeakMeter

IID_IAudioTreble

IID_IAudioVolumeLevel

IID_IDeviceSpecificProperty

IID_IKsFormatSupport

IID_IKsJackDescription

IID_IKsJackDescription2

For more information, see Remarks.

### -param ppvObject [out]

Pointer to a pointer variable into which the method writes the address of the interface that is specified by parameter <i>refiid</i>. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>Activate</b> call fails,  <i>*ppObject</i> is <b>NULL</b>.

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
The CLSCTX_INPROC_SERVER bit in <i>dwClsContext</i> is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppvObject</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The part object does not support the requested interface.

</td>
</tr>
</table>

## -remarks

The <b>Activate</b> method supports the following function-specific control interfaces:

<ul>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioautogaincontrol">IAudioAutoGainControl</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiobass">IAudioBass</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioinputselector">IAudioInputSelector</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioloudness">IAudioLoudness</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomidrange">IAudioMidrange</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomute">IAudioMute</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiooutputselector">IAudioOutputSelector</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiopeakmeter">IAudioPeakMeter</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiotreble">IAudioTreble</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicespecificproperty">IDeviceSpecificProperty</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksformatsupport">IKsFormatSupport</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription">IKsJackDescription</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription2">IKsJackDescription2</a>
</li>
</ul>
To obtain the interface ID of the function-specific control interface of a part, call the part's <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolinterface-getiid">IControlInterface::GetIID</a> method. To obtain the interface ID of a function-specific control interface type, use the <b>__uuidof</b> operator. For example, the interface ID of <b>IAudioAutoGainControl</b> is defined as follows:


``` syntax

const IID IID_IAudioAutoGainControl  __uuidof(IAudioAutoGainControl)

```

For more information about the <b>__uuidof</b> operator, see the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolinterface-getiid">IControlInterface::GetIID</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>
