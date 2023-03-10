---
UID: NF:devicetopology.IPart.RegisterControlChangeCallback
title: IPart::RegisterControlChangeCallback (devicetopology.h)
description: The RegisterControlChangeCallback method registers the IControlChangeNotify interface, which the client implements to receive notifications of status changes in this part.
helpviewer_keywords: ["IPart interface [Core Audio]","RegisterControlChangeCallback method","IPart.RegisterControlChangeCallback","IPart::RegisterControlChangeCallback","IPartRegisterControlChangeCallback","RegisterControlChangeCallback","RegisterControlChangeCallback method [Core Audio]","RegisterControlChangeCallback method [Core Audio]","IPart interface","coreaudio.ipart_registercontrolchangecallback","devicetopology/IPart::RegisterControlChangeCallback"]
old-location: coreaudio\ipart_registercontrolchangecallback.htm
tech.root: CoreAudio
ms.assetid: 58cf52c9-20ee-46c4-926e-c374a4f42240
ms.date: 12/05/2018
ms.keywords: IPart interface [Core Audio],RegisterControlChangeCallback method, IPart.RegisterControlChangeCallback, IPart::RegisterControlChangeCallback, IPartRegisterControlChangeCallback, RegisterControlChangeCallback, RegisterControlChangeCallback method [Core Audio], RegisterControlChangeCallback method [Core Audio],IPart interface, coreaudio.ipart_registercontrolchangecallback, devicetopology/IPart::RegisterControlChangeCallback
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
 - IPart::RegisterControlChangeCallback
 - devicetopology/IPart::RegisterControlChangeCallback
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
 - IPart.RegisterControlChangeCallback
---

# IPart::RegisterControlChangeCallback


## -description

The <b>RegisterControlChangeCallback</b> method registers the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interface, which the client implements to receive notifications of status changes in this part.

## -parameters

### -param riid [in]

The function-specific control interface that is to be monitored for control changes. For more information, see Remarks.

### -param pNotify [in]

Pointer to the client's <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interface. If the method succeeds, it calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the client's <b>IControlChangeNotify</b> interface.

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
Parameter <i>riid</i> is not a valid control-interface identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pNotify</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Set parameter <i>riid</i> to one of the following GUID values:

<ul>
<li>IID_IAudioAutoGainControl</li>
<li>IID_IAudioBass</li>
<li>IID_IAudioChannelConfig</li>
<li>IID_IAudioInputSelector</li>
<li>IID_IAudioLoudness</li>
<li>IID_IAudioMidrange</li>
<li>IID_IAudioMute</li>
<li>IID_IAudioOutputSelector</li>
<li>IID_IAudioPeakMeter</li>
<li>IID_IAudioTreble</li>
<li>IID_IAudioVolumeLevel</li>
<li>IID_IDeviceSpecificProperty</li>
<li>IID_IKsFormatSupport</li>
<li>IID_IKsJackDescription</li>
</ul>
To obtain the interface ID of the function-specific control interface for a part, call the part's <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolinterface-getiid">IControlInterface::GetIID</a> method. To obtain the interface ID of a function-specific control interface type, use the <b>__uuidof</b> operator. For example, the interface ID of <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioautogaincontrol">IAudioAutoGainControl</a> is defined as follows:


``` syntax

const IID IID_IAudioAutoGainControl  __uuidof(IAudioAutoGainControl)

```

For more information about the <b>__uuidof</b> operator, see the Windows SDK documentation.

Before the client releases its final reference to the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interface, it should call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-unregistercontrolchangecallback">IPart::UnregisterControlChangeCallback</a> method to unregister the interface. Otherwise, the application leaks the resources held by the <b>IControlChangeNotify</b> and <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> objects. Note that <b>RegisterControlChangeCallback</b> calls the client's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IControlChangeNotify::AddRef</a> method, and <b>UnregisterControlChangeCallback</b> calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IControlChangeNotify::Release</a> method. If the client errs by releasing its reference to the <b>IControlChangeNotify</b> interface before calling <b>UnregisterControlChangeCallback</b>, the <b>IPart</b> object never releases its reference to the <b>IControlChangeNotify</b> interface. For example, a poorly designed <b>IControlChangeNotify</b> implementation might call <b>UnregisterControlChangeCallback</b> from the destructor for the <b>IControlChangeNotify</b> object. In this case, the client will not call <b>UnregisterControlChangeCallback</b> until the <b>IPart</b> object releases its reference to the <b>IControlChangeNotify</b> interface, and the <b>IPart</b> object will not release its reference to the <b>IControlChangeNotify</b> interface until the client calls <b>UnregisterControlChangeCallback</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolinterface-getiid">IControlInterface::GetIID</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-unregistercontrolchangecallback">IPart::UnregisterControlChangeCallback</a>
