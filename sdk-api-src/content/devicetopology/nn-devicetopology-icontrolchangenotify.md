---
UID: NN:devicetopology.IControlChangeNotify
title: IControlChangeNotify
author: windows-sdk-content
description: The IControlChangeNotify interface provides notifications when the status of a part (connector or subunit) changes.
old-location: coreaudio\icontrolchangenotify.htm
tech.root: CoreAudio
ms.assetid: e50e13c2-1ef3-46f6-8c53-f99cc1631a79
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IControlChangeNotify, IControlChangeNotify interface [Core Audio], IControlChangeNotify interface [Core Audio],described, coreaudio.icontrolchangenotify, devicetopology/IControlChangeNotify
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IControlChangeNotify interface


## -description



The <b>IControlChangeNotify</b> interface provides notifications when the status of a part (connector or subunit) changes. Unlike the other interfaces in this section, which are implemented by the DeviceTopology API, the <b>IControlChangeNotify</b> interface must be implemented by a client. To receive notifications, the client passes a pointer to its <b>IControlChangeNotify</b> interface instance as a parameter to the <a href="https://msdn.microsoft.com/58cf52c9-20ee-46c4-926e-c374a4f42240">IPart::RegisterControlChangeCallback</a> method.

After registering its <b>IControlChangeNotify</b> interface, the client receives event notifications in the form of callbacks through the <b>OnNotify</b> method in the interface.

In implementing the <b>IControlChangeNotify</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="https://msdn.microsoft.com/d3341421-6dab-43f3-87a8-83ee8a986a04">IPart::UnregisterControlChangeCallback</a> method during an event callback.</li>
<li>The client should never release the final reference on an MMDevice API object during an event callback.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IControlChangeNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IControlChangeNotify</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a2f32cb9-3c8b-4b44-96a2-dd70afcca71a">OnNotify</a>
</td>
<td align="left" width="63%">
Notifies the client when the status of a part (connector or subunit) changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/58cf52c9-20ee-46c4-926e-c374a4f42240">IPart::RegisterControlChangeCallback</a>



<a href="https://msdn.microsoft.com/d3341421-6dab-43f3-87a8-83ee8a986a04">IPart::UnregisterControlChangeCallback</a>
 

 

