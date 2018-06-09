---
UID: NF:devicetopology.IPart.RegisterControlChangeCallback
title: IPart::RegisterControlChangeCallback
author: windows-sdk-content
description: The RegisterControlChangeCallback method registers the IControlChangeNotify interface, which the client implements to receive notifications of status changes in this part.
old-location: coreaudio\ipart_registercontrolchangecallback.htm
old-project: CoreAudio
ms.assetid: 58cf52c9-20ee-46c4-926e-c374a4f42240
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IPart interface [Core Audio],RegisterControlChangeCallback method, IPart.RegisterControlChangeCallback, IPart::RegisterControlChangeCallback, IPartRegisterControlChangeCallback, RegisterControlChangeCallback, RegisterControlChangeCallback method [Core Audio], RegisterControlChangeCallback method [Core Audio],IPart interface, coreaudio.ipart_registercontrolchangecallback, devicetopology/IPart::RegisterControlChangeCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPart.RegisterControlChangeCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPart::RegisterControlChangeCallback


## -description



The <b>RegisterControlChangeCallback</b> method registers the <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interface, which the client implements to receive notifications of status changes in this part.




## -parameters




### -param riid [in]

The function-specific control interface that is to be monitored for control changes. For more information, see Remarks.


### -param pNotify [in]

Pointer to the client's <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interface. If the method succeeds, it calls the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method on the client's <b>IControlChangeNotify</b> interface.


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
To obtain the interface ID of the function-specific control interface for a part, call the part's <a href="https://msdn.microsoft.com/c6d46f37-6b9a-4d20-8a97-9fb5284dbc42">IControlInterface::GetIID</a> method. To obtain the interface ID of a function-specific control interface type, use the <b>__uuidof</b> operator. For example, the interface ID of <a href="https://msdn.microsoft.com/f21e27e6-f3a0-418a-ad2e-e3e104dd6da2">IAudioAutoGainControl</a> is defined as follows:

<pre class="syntax" xml:space="preserve"><code>
const IID IID_IAudioAutoGainControl  __uuidof(IAudioAutoGainControl)
</code></pre>
For more information about the <b>__uuidof</b> operator, see the Windows SDK documentation.

Before the client releases its final reference to the <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interface, it should call the <a href="https://msdn.microsoft.com/d3341421-6dab-43f3-87a8-83ee8a986a04">IPart::UnregisterControlChangeCallback</a> method to unregister the interface. Otherwise, the application leaks the resources held by the <b>IControlChangeNotify</b> and <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> objects. Note that <b>RegisterControlChangeCallback</b> calls the client's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IControlChangeNotify::AddRef</a> method, and <b>UnregisterControlChangeCallback</b> calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IControlChangeNotify::Release</a> method. If the client errs by releasing its reference to the <b>IControlChangeNotify</b> interface before calling <b>UnregisterControlChangeCallback</b>, the <b>IPart</b> object never releases its reference to the <b>IControlChangeNotify</b> interface. For example, a poorly designed <b>IControlChangeNotify</b> implementation might call <b>UnregisterControlChangeCallback</b> from the destructor for the <b>IControlChangeNotify</b> object. In this case, the client will not call <b>UnregisterControlChangeCallback</b> until the <b>IPart</b> object releases its reference to the <b>IControlChangeNotify</b> interface, and the <b>IPart</b> object will not release its reference to the <b>IControlChangeNotify</b> interface until the client calls <b>UnregisterControlChangeCallback</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify Interface</a>



<a href="https://msdn.microsoft.com/c6d46f37-6b9a-4d20-8a97-9fb5284dbc42">IControlInterface::GetIID</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/d3341421-6dab-43f3-87a8-83ee8a986a04">IPart::UnregisterControlChangeCallback</a>
 

 

