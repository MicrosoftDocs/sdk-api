---
UID: NF:devicetopology.IControlInterface.GetIID
title: IControlInterface::GetIID
author: windows-sdk-content
description: The GetIID method gets the interface ID of the function-specific control interface of the part.
old-location: coreaudio\icontrolinterface_getiid.htm
old-project: CoreAudio
ms.assetid: c6d46f37-6b9a-4d20-8a97-9fb5284dbc42
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetIID, GetIID method [Core Audio], GetIID method [Core Audio],IControlInterface interface, IControlInterface interface [Core Audio],GetIID method, IControlInterface.GetIID, IControlInterface::GetIID, IControlInterfaceGetIID, coreaudio.icontrolinterface_getiid, devicetopology/IControlInterface::GetIID
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
 - IControlInterface.GetIID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



An object that represents a part (connector or subunit) has two control interfaces. The first is a generic control interface, <a href="https://msdn.microsoft.com/fdd91f65-e45c-4f14-a55c-a44be1661950">IControlInterface</a>, which has methods that are common to all types of controls. The second is a function-specific control interface that has methods that apply to a particular type of control. The <b>GetIID</b> method gets the interface ID of the second control interface. The client can supply this interface ID to the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method to create an instance of the part's function-specific interface.

The method gets one of the function-specific interface IDs shown in the following table.

<table>
<tr>
<th>
              Interface ID
            </th>
<th>
              Interface name
            </th>
</tr>
<tr>
<td>IID_IAudioAutoGainControl</td>
<td>
<a href="https://msdn.microsoft.com/f21e27e6-f3a0-418a-ad2e-e3e104dd6da2">IAudioAutoGainControl</a>
</td>
</tr>
<tr>
<td>IID_IAudioBass</td>
<td>
<a href="https://msdn.microsoft.com/036ca996-8612-4905-9afa-a4c3b4624652">IAudioBass</a>
</td>
</tr>
<tr>
<td>IID_IAudioChannelConfig</td>
<td>
<a href="https://msdn.microsoft.com/b8e54e9e-a6eb-46e6-a71c-ff498c7e8f47">IAudioChannelConfig</a>
</td>
</tr>
<tr>
<td>IID_IAudioInputSelector</td>
<td>
<a href="https://msdn.microsoft.com/6f5ce9c0-39e4-4fab-910c-9a11b90fcde7">IAudioInputSelector</a>
</td>
</tr>
<tr>
<td>IID_IAudioLoudness</td>
<td>
<a href="https://msdn.microsoft.com/c182d6ae-c55b-4e3b-9639-7c2f2f7d826d">IAudioLoudness</a>
</td>
</tr>
<tr>
<td>IID_IAudioMidrange</td>
<td>
<a href="https://msdn.microsoft.com/d2d93dba-1867-4c3a-9cd1-60842bf8311d">IAudioMidrange</a>
</td>
</tr>
<tr>
<td>IID_IAudioMute</td>
<td>
<a href="https://msdn.microsoft.com/53d49af7-81c3-4e75-ba06-dcee34d84292">IAudioMute</a>
</td>
</tr>
<tr>
<td>IID_IAudioOutputSelector</td>
<td>
<a href="https://msdn.microsoft.com/571a44b6-972f-4d75-a31f-0e02cf728764">IAudioOutputSelector</a>
</td>
</tr>
<tr>
<td>IID_IAudioPeakMeter</td>
<td>
<a href="https://msdn.microsoft.com/524d83ff-4303-448c-a070-58d17dec03ba">IAudioPeakMeter</a>
</td>
</tr>
<tr>
<td>IID_IAudioTreble</td>
<td>
<a href="https://msdn.microsoft.com/3ace174e-c21c-41e7-9830-80d247d8437f">IAudioTreble</a>
</td>
</tr>
<tr>
<td>IID_IAudioVolumeLevel</td>
<td>
<a href="https://msdn.microsoft.com/5e7d7111-e4b0-43b3-af35-9878d1a19e5f">IAudioVolumeLevel</a>
</td>
</tr>
<tr>
<td>IID_IDeviceSpecificProperty</td>
<td>
<a href="https://msdn.microsoft.com/52873fe2-7f59-4a30-b526-cbefa27a81bb">IDeviceSpecificProperty</a>
</td>
</tr>
<tr>
<td>IID_IKsFormatSupport</td>
<td>
<a href="https://msdn.microsoft.com/53a29b57-1650-4e4d-b9d2-95307063a733">IKsFormatSupport</a>
</td>
</tr>
<tr>
<td>IID_IKsJackDescription</td>
<td>
<a href="https://msdn.microsoft.com/0ca9e719-7179-4302-99ff-df137141f58f">IKsJackDescription</a>
</td>
</tr>
</table>
 

To obtain the interface ID of an interface, use the <b>__uuidof</b> operator. For example, the interface ID of the <b>IAudioAutoGainControl</b> interface is defined as follows:

<pre class="syntax" xml:space="preserve"><code>
const IID IID_IAudioAutoGainControl  __uuidof(IAudioAutoGainControl)
</code></pre>
For more information about the <b>__uuidof</b> operator, see the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdd91f65-e45c-4f14-a55c-a44be1661950">IControlInterface Interface</a>
 

 

