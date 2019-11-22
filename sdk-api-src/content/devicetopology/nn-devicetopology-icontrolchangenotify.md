---
UID: NN:devicetopology.IControlChangeNotify
title: IControlChangeNotify (devicetopology.h)

description: The IControlChangeNotify interface provides notifications when the status of a part (connector or subunit) changes.
old-location: coreaudio\icontrolchangenotify.htm
tech.root: CoreAudio
ms.assetid: e50e13c2-1ef3-46f6-8c53-f99cc1631a79

ms.date: 12/05/2018
ms.keywords: IControlChangeNotify, IControlChangeNotify interface [Core Audio], IControlChangeNotify interface [Core Audio],described, coreaudio.icontrolchangenotify, devicetopology/IControlChangeNotify
ms.topic: interface
f1_keywords: 
 - "devicetopology/IControlChangeNotify"
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
 - IControlChangeNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IControlChangeNotify interface


## -description



The <b>IControlChangeNotify</b> interface provides notifications when the status of a part (connector or subunit) changes. Unlike the other interfaces in this section, which are implemented by the DeviceTopology API, the <b>IControlChangeNotify</b> interface must be implemented by a client. To receive notifications, the client passes a pointer to its <b>IControlChangeNotify</b> interface instance as a parameter to the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">IPart::RegisterControlChangeCallback</a> method.

After registering its <b>IControlChangeNotify</b> interface, the client receives event notifications in the form of callbacks through the <b>OnNotify</b> method in the interface.

In implementing the <b>IControlChangeNotify</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-unregistercontrolchangecallback">IPart::UnregisterControlChangeCallback</a> method during an event callback.</li>
<li>The client should never release the final reference on an MMDevice API object during an event callback.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IControlChangeNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IControlChangeNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IControlChangeNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">OnNotify</a>
</td>
<td align="left" width="63%">
Notifies the client when the status of a part (connector or subunit) changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">IPart::RegisterControlChangeCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-unregistercontrolchangecallback">IPart::UnregisterControlChangeCallback</a>
 

 

