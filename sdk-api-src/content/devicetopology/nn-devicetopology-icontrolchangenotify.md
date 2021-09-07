---
UID: NN:devicetopology.IControlChangeNotify
title: IControlChangeNotify (devicetopology.h)
description: The IControlChangeNotify interface provides notifications when the status of a part (connector or subunit) changes.
helpviewer_keywords: ["IControlChangeNotify","IControlChangeNotify interface [Core Audio]","IControlChangeNotify interface [Core Audio]","described","coreaudio.icontrolchangenotify","devicetopology/IControlChangeNotify"]
old-location: coreaudio\icontrolchangenotify.htm
tech.root: CoreAudio
ms.assetid: e50e13c2-1ef3-46f6-8c53-f99cc1631a79
ms.date: 12/05/2018
ms.keywords: IControlChangeNotify, IControlChangeNotify interface [Core Audio], IControlChangeNotify interface [Core Audio],described, coreaudio.icontrolchangenotify, devicetopology/IControlChangeNotify
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
 - IControlChangeNotify
 - devicetopology/IControlChangeNotify
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
 - IControlChangeNotify
---

# IControlChangeNotify interface


## -description

The <b>IControlChangeNotify</b> interface provides notifications when the status of a part (connector or subunit) changes. Unlike the other interfaces in this section, which are implemented by the DeviceTopology API, the <b>IControlChangeNotify</b> interface must be implemented by a client. To receive notifications, the client passes a pointer to its <b>IControlChangeNotify</b> interface instance as a parameter to the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">IPart::RegisterControlChangeCallback</a> method.

After registering its <b>IControlChangeNotify</b> interface, the client receives event notifications in the form of callbacks through the <b>OnNotify</b> method in the interface.

In implementing the <b>IControlChangeNotify</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-unregistercontrolchangecallback">IPart::UnregisterControlChangeCallback</a> method during an event callback.</li>
<li>The client should never release the final reference on an MMDevice API object during an event callback.</li>
</ul>

## -inheritance

The <b>IControlChangeNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IControlChangeNotify</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">IPart::RegisterControlChangeCallback</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-unregistercontrolchangecallback">IPart::UnregisterControlChangeCallback</a>
