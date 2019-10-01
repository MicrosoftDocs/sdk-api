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
f1_keywords: 
 - "devicetopology/IPartsList"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPartsList interface


## -description



The <b>IPartsList</b> interface represents a list of parts, each of which is an object with an <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface that represents a connector or subunit. A client obtains a reference to an <b>IPartsList</b> interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsincoming">IPart::EnumPartsIncoming</a>, <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsoutgoing">IPart::EnumPartsOutgoing</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsignalpath">IDeviceTopology::GetSignalPath</a> method.

For a code example that uses the <b>IPartsList</b> interface, see the implementation of the SelectCaptureDevice function in <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPartsList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPartsList</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of parts in the parts list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getpart">GetPart</a>
</td>
<td align="left" width="63%">
Gets a part from the parts list.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsignalpath">IDeviceTopology::GetSignalPath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsincoming">IPart::EnumPartsIncoming</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsoutgoing">IPart::EnumPartsOutgoing</a>
 

 

