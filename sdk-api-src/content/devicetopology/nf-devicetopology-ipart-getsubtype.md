---
UID: NF:devicetopology.IPart.GetSubType
title: IPart::GetSubType (devicetopology.h)
description: The GetSubType method gets the part subtype of this part.
helpviewer_keywords: ["GetSubType","GetSubType method [Core Audio]","GetSubType method [Core Audio]","IPart interface","IPart interface [Core Audio]","GetSubType method","IPart.GetSubType","IPart::GetSubType","IPartGetSubType","coreaudio.ipart_getsubtype","devicetopology/IPart::GetSubType"]
old-location: coreaudio\ipart_getsubtype.htm
tech.root: CoreAudio
ms.assetid: 456aaafb-1e68-4a3a-b27b-c6f6f89dc17b
ms.date: 12/05/2018
ms.keywords: GetSubType, GetSubType method [Core Audio], GetSubType method [Core Audio],IPart interface, IPart interface [Core Audio],GetSubType method, IPart.GetSubType, IPart::GetSubType, IPartGetSubType, coreaudio.ipart_getsubtype, devicetopology/IPart::GetSubType
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
 - IPart::GetSubType
 - devicetopology/IPart::GetSubType
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
 - IPart.GetSubType
---

# IPart::GetSubType


## -description

The <b>GetSubType</b> method gets the part subtype of this part.

## -parameters

### -param pSubType [out]

Pointer to a GUID variable into which the method writes the subtype GUID for this part.

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
Pointer <i>pSubType</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method typically retrieves one of the KSNODETYPE_<i>Xxx</i> GUID values from header file Ksmedia.h, although some custom drivers might provide other GUID values. For more information about KSNODETYPE_<i>Xxx</i> GUIDs, see the Windows DDK documentation.

As explained in <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>, a part can be either a connector or a subunit.

For a part that is a connector, this method retrieves the pin-category GUID that the driver has assigned to the connector. The following are examples of pin-category GUIDs:

<ul>
<li>KSNODETYPE_ANALOG_CONNECTOR, if the connector is part of the data path to or from an analog device such as a microphone or speakers.</li>
<li>KSNODETYPE_SPDIF_INTERFACE, if the connector is part of the data path to or from an S/PDIF port.</li>
</ul>
For more information, see the discussion of the pin-category property, KSPROPERTY_PIN_CATEGORY, in the Windows DDK documentation.

For a part that is a subunit, this method retrieves a subtype GUID that indicates the stream-processing function that the subunit performs. For example, for a volume-control subunit, the method retrieves GUID value KSNODETYPE_VOLUME.

The following table lists some of the subtype GUIDs that can be retrieved by the <b>GetSubType</b> method for a subunit.

<table>
<tr>
<th>Subtype GUID
            </th>
<th>Control interface
            </th>
<th>Required or optional
            </th>
</tr>
<tr>
<td>KSNODETYPE_3D_EFFECTS</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig</a>
</td>
<td>Optional</td>
</tr>
<tr>
<td>KSNODETYPE_AGC</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioautogaincontrol">IAudioAutoGainControl</a>
</td>
<td>Required</td>
</tr>
<tr>
<td>KSNODETYPE_DAC</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig</a>
</td>
<td>Optional</td>
</tr>
<tr>
<td>KSNODETYPE_DEMUX</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiooutputselector">IAudioOutputSelector</a>
</td>
<td>Required</td>
</tr>
<tr>
<td>KSNODETYPE_DEV_SPECIFIC</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicespecificproperty">IDeviceSpecificProperty</a>
</td>
<td>Required</td>
</tr>
<tr>
<td>KSNODETYPE_LOUDNESS</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioloudness">IAudioLoudness</a>
</td>
<td>Required</td>
</tr>
<tr>
<td>KSNODETYPE_MUTE</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomute">IAudioMute</a>
</td>
<td>Required</td>
</tr>
<tr>
<td>KSNODETYPE_MUX</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioinputselector">IAudioInputSelector</a>
</td>
<td>Required</td>
</tr>
<tr>
<td>KSNODETYPE_PEAKMETER</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiopeakmeter">IAudioPeakMeter</a>
</td>
<td>Required</td>
</tr>
<tr>
<td>KSNODETYPE_PROLOGIC_DECODER</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig</a>
</td>
<td>Optional</td>
</tr>
<tr>
<td>KSNODETYPE_TONE</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiobass">IAudioBass</a>

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomidrange">IAudioMidrange</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiotreble">IAudioTreble</a>


</td>
<td>OptionalOptional

Optional

</td>
</tr>
<tr>
<td>KSNODETYPE_VOLUME</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig</a>

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel</a>


</td>
<td>OptionalRequired

</td>
</tr>
</table>
 

In the preceding table, the middle column lists the control interfaces that are supported by subunits of the subtype specified in the left column. The right column indicates whether the subunit's support for a control interface is required or optional. If support is required, an application can rely on a subunit of the specified subtype to support the control interface. If support is optional, a subunit of the specified subtype can, but does not necessarily, support the control interface.

The control interfaces in the preceding table provide convenient access to the properties of subunits. However, some subunits have properties for which no corresponding control interfaces exist. Applications can access these properties through the <a href="/windows-hardware/drivers/ddi/content/ksproxy/nn-ksproxy-ikscontrol">IKsControl</a> interface. For more information, see <a href="/windows/desktop/CoreAudio/using-the-ikscontrol-interface-to-access-audio-properties">Using the IKsControl Interface to Access Audio Properties</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>