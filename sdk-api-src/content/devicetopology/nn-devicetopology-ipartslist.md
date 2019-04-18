---
UID: NN:devicetopology.IPartsList
title: IPartsList (devicetopology.h)
author: windows-sdk-content
description: The IPartsList interface represents a list of parts, each of which is an object with an IPart interface that represents a connector or subunit.
old-location: coreaudio\ipartslist.htm
tech.root: CoreAudio
ms.assetid: 3ac48781-90c2-4b23-aa68-3453091bde61
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPartsList, IPartsList interface [Core Audio], IPartsList interface [Core Audio],described, coreaudio.ipartslist, devicetopology/IPartsList
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPartsList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPartsList interface


## -description



The <b>IPartsList</b> interface represents a list of parts, each of which is an object with an <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> interface that represents a connector or subunit. A client obtains a reference to an <b>IPartsList</b> interface by calling the <a href="https://msdn.microsoft.com/0d74837e-12d1-4d94-941e-6a81aeac1151">IPart::EnumPartsIncoming</a>, <a href="https://msdn.microsoft.com/f1892e6d-a2d8-45c7-8a36-6040f4538c1e">IPart::EnumPartsOutgoing</a>, or <a href="https://msdn.microsoft.com/3f32ba6a-a82c-4c2c-8433-ebedd8799615">IDeviceTopology::GetSignalPath</a> method.

For a code example that uses the <b>IPartsList</b> interface, see the implementation of the SelectCaptureDevice function in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPartsList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPartsList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPartsList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78ca8592-f687-4194-873b-83640c6e72da">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of parts in the parts list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/505e2412-2849-4e64-9751-ce68831823b8">GetPart</a>
</td>
<td align="left" width="63%">
Gets a part from the parts list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/3f32ba6a-a82c-4c2c-8433-ebedd8799615">IDeviceTopology::GetSignalPath</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/0d74837e-12d1-4d94-941e-6a81aeac1151">IPart::EnumPartsIncoming</a>



<a href="https://msdn.microsoft.com/f1892e6d-a2d8-45c7-8a36-6040f4538c1e">IPart::EnumPartsOutgoing</a>
 

 

