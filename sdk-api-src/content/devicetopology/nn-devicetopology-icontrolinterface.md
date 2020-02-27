---
UID: NN:devicetopology.IControlInterface
title: IControlInterface (devicetopology.h)
description: The IControlInterface interface represents a control interface on a part (connector or subunit) in a device topology. The client obtains a reference to a part's IControlInterface interface by calling the IPart::GetControlInterface method.
old-location: coreaudio\icontrolinterface.htm
tech.root: CoreAudio
ms.assetid: fdd91f65-e45c-4f14-a55c-a44be1661950
ms.date: 12/05/2018
ms.keywords: IControlInterface, IControlInterface interface [Core Audio], IControlInterface interface [Core Audio],described, coreaudio.icontrolinterface, devicetopology/IControlInterface
f1_keywords:
- devicetopology/IControlInterface
dev_langs:
- c++
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
- IControlInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IControlInterface interface


## -description



The <b>IControlInterface</b> interface represents a control interface on a part (connector or subunit) in a <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">device topology</a>. The client obtains a reference to a part's <b>IControlInterface</b> interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getcontrolinterface">IPart::GetControlInterface</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IControlInterface</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IControlInterface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IControlInterface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-icontrolinterface-getiid">GetIID</a>
</td>
<td align="left" width="63%">
Gets the interface ID of the function-specific control interface of the part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-icontrolinterface-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the audio function that the control interface encapsulates.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getcontrolinterface">IPart::GetControlInterface</a>
 

 

