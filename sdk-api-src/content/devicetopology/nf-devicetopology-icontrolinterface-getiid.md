---
UID: NF:devicetopology.IControlInterface.GetIID
title: IControlInterface::GetIID (devicetopology.h)
description: The GetIID method gets the interface ID of the function-specific control interface of the part.
helpviewer_keywords: ["GetIID","GetIID method [Core Audio]","GetIID method [Core Audio]","IControlInterface interface","IControlInterface interface [Core Audio]","GetIID method","IControlInterface.GetIID","IControlInterface::GetIID","IControlInterfaceGetIID","coreaudio.icontrolinterface_getiid","devicetopology/IControlInterface::GetIID"]
old-location: coreaudio\icontrolinterface_getiid.htm
tech.root: CoreAudio
ms.assetid: c6d46f37-6b9a-4d20-8a97-9fb5284dbc42
ms.date: 12/05/2018
ms.keywords: GetIID, GetIID method [Core Audio], GetIID method [Core Audio],IControlInterface interface, IControlInterface interface [Core Audio],GetIID method, IControlInterface.GetIID, IControlInterface::GetIID, IControlInterfaceGetIID, coreaudio.icontrolinterface_getiid, devicetopology/IControlInterface::GetIID
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
 - IControlInterface::GetIID
 - devicetopology/IControlInterface::GetIID
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
 - IControlInterface.GetIID
---

# IControlInterface::GetIID


## -description

The <b>GetIID</b> method gets the interface ID of the function-specific control interface of the part.

## -parameters

### -param pIID [out]

Pointer to a GUID variable into which the method writes the interface ID of the function-specific control interface of the part. For more information, see Remarks.

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
Pointer <i>pIID</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

An object that represents a part (connector or subunit) has two control interfaces. The first is a generic control interface, <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolinterface">IControlInterface</a>, which has methods that are common to all types of controls. The second is a function-specific control interface that has methods that apply to a particular type of control. The <b>GetIID</b> method gets the interface ID of the second control interface. The client can supply this interface ID to the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method to create an instance of the part's function-specific interface.

The method gets one of the function-specific interface IDs shown in the following table.

<table>
<tr>
<th>Interface ID
            </th>
<th>Interface name
            </th>
</tr>
<tr>
<td>IID_IAudioAutoGainControl</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioautogaincontrol">IAudioAutoGainControl</a>
</td>
</tr>
<tr>
<td>IID_IAudioBass</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiobass">IAudioBass</a>
</td>
</tr>
<tr>
<td>IID_IAudioChannelConfig</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig</a>
</td>
</tr>
<tr>
<td>IID_IAudioInputSelector</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioinputselector">IAudioInputSelector</a>
</td>
</tr>
<tr>
<td>IID_IAudioLoudness</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioloudness">IAudioLoudness</a>
</td>
</tr>
<tr>
<td>IID_IAudioMidrange</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomidrange">IAudioMidrange</a>
</td>
</tr>
<tr>
<td>IID_IAudioMute</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomute">IAudioMute</a>
</td>
</tr>
<tr>
<td>IID_IAudioOutputSelector</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiooutputselector">IAudioOutputSelector</a>
</td>
</tr>
<tr>
<td>IID_IAudioPeakMeter</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiopeakmeter">IAudioPeakMeter</a>
</td>
</tr>
<tr>
<td>IID_IAudioTreble</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiotreble">IAudioTreble</a>
</td>
</tr>
<tr>
<td>IID_IAudioVolumeLevel</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel</a>
</td>
</tr>
<tr>
<td>IID_IDeviceSpecificProperty</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicespecificproperty">IDeviceSpecificProperty</a>
</td>
</tr>
<tr>
<td>IID_IKsFormatSupport</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksformatsupport">IKsFormatSupport</a>
</td>
</tr>
<tr>
<td>IID_IKsJackDescription</td>
<td>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription">IKsJackDescription</a>
</td>
</tr>
</table>
 

To obtain the interface ID of an interface, use the <b>__uuidof</b> operator. For example, the interface ID of the <b>IAudioAutoGainControl</b> interface is defined as follows:


``` syntax

const IID IID_IAudioAutoGainControl  __uuidof(IAudioAutoGainControl)

```

For more information about the <b>__uuidof</b> operator, see the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolinterface">IControlInterface Interface</a>
