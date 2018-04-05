---
UID: NF:devicetopology.IPart.Activate
title: IPart::Activate method
author: windows-driver-content
description: The Activate method activates a function-specific interface on a connector or subunit.
old-location: coreaudio\ipart_activate.htm
old-project: CoreAudio
ms.assetid: 72e08a30-65c0-437b-9932-110ba48a2376
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: Activate method [Core Audio], Activate method [Core Audio], IPart interface, Activate,IPart.Activate, IPart, IPart interface [Core Audio], Activate method, IPart::Activate, IPartActivate, coreaudio.ipart_activate, devicetopology/IPart::Activate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ConnectorType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Devicetopology.h
api_name:
-	IPart.Activate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPart::Activate method


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
<a href="https://msdn.microsoft.com/f21e27e6-f3a0-418a-ad2e-e3e104dd6da2">IAudioAutoGainControl</a>
</li>
<li>
<a href="https://msdn.microsoft.com/036ca996-8612-4905-9afa-a4c3b4624652">IAudioBass</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8e54e9e-a6eb-46e6-a71c-ff498c7e8f47">IAudioChannelConfig</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6f5ce9c0-39e4-4fab-910c-9a11b90fcde7">IAudioInputSelector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c182d6ae-c55b-4e3b-9639-7c2f2f7d826d">IAudioLoudness</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d2d93dba-1867-4c3a-9cd1-60842bf8311d">IAudioMidrange</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53d49af7-81c3-4e75-ba06-dcee34d84292">IAudioMute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/571a44b6-972f-4d75-a31f-0e02cf728764">IAudioOutputSelector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/524d83ff-4303-448c-a070-58d17dec03ba">IAudioPeakMeter</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ace174e-c21c-41e7-9830-80d247d8437f">IAudioTreble</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e7d7111-e4b0-43b3-af35-9878d1a19e5f">IAudioVolumeLevel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/52873fe2-7f59-4a30-b526-cbefa27a81bb">IDeviceSpecificProperty</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53a29b57-1650-4e4d-b9d2-95307063a733">IKsFormatSupport</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0ca9e719-7179-4302-99ff-df137141f58f">IKsJackDescription</a>
</li>
</ul>
To obtain the interface ID of the function-specific control interface of a part, call the part's <a href="https://msdn.microsoft.com/c6d46f37-6b9a-4d20-8a97-9fb5284dbc42">IControlInterface::GetIID</a> method. To obtain the interface ID of a function-specific control interface type, use the <b>__uuidof</b> operator. For example, the interface ID of <b>IAudioAutoGainControl</b> is defined as follows:

<pre class="syntax" xml:space="preserve"><code>
const IID IID_IAudioAutoGainControl  __uuidof(IAudioAutoGainControl)
</code></pre>
For more information about the <b>__uuidof</b> operator, see the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/c6d46f37-6b9a-4d20-8a97-9fb5284dbc42">IControlInterface::GetIID</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 

