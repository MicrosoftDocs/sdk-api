---
UID: NN:devicetopology.IDeviceSpecificProperty
title: IDeviceSpecificProperty
author: windows-sdk-content
description: The IDeviceSpecificProperty interface provides access to the control value of a device-specific hardware control.
old-location: coreaudio\idevicespecificproperty.htm
old-project: CoreAudio
ms.assetid: 52873fe2-7f59-4a30-b526-cbefa27a81bb
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDeviceSpecificProperty, IDeviceSpecificProperty interface [Core Audio], IDeviceSpecificProperty interface [Core Audio],described, coreaudio.idevicespecificproperty, devicetopology/IDeviceSpecificProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Devicetopology.h
api_name:
-	IDeviceSpecificProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDeviceSpecificProperty interface


## -description



The <b>IDeviceSpecificProperty</b> interface provides access to the control value of a device-specific hardware control. A client obtains a reference to an <b>IDeviceSpecificProperty</b> interface of a part by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b> IID_IDeviceSpecificProperty. The call to <b>IPart::Activate</b> succeeds only if the part supports the <b>IDeviceSpecificProperty</b> interface. A part supports this interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other interface in the DeviceTopology API.

Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name. The client can obtain this information by calling the <a href="https://msdn.microsoft.com/79af1dce-b946-4ef2-af36-4437603966da">IPart::GetPartType</a>, <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a>, and <a href="https://msdn.microsoft.com/a583f445-ebb2-4072-a272-6f186aef71b3">IPart::GetName</a> methods.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IDeviceSpecificProperty</b> interface provides convenient access to the KSPROPERTY_AUDIO_DEV_SPECIFIC property of a subunit that has a subtype GUID value of KSNODETYPE_DEV_SPECIFIC. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeviceSpecificProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDeviceSpecificProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeviceSpecificProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16ca72b5-2de2-4644-9c64-cdc69a9b2c51">Get4BRange</a>
</td>
<td align="left" width="63%">
Gets the 4-byte range of the device-specific property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Gets the data type of the device-specific property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Gets the value of the device-specific property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of the device-specific property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>



<a href="https://msdn.microsoft.com/a583f445-ebb2-4072-a272-6f186aef71b3">IPart::GetName</a>



<a href="https://msdn.microsoft.com/79af1dce-b946-4ef2-af36-4437603966da">IPart::GetPartType</a>



<a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a>
 

 

