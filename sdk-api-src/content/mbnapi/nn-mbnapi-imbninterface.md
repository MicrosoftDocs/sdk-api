---
UID: NN:mbnapi.IMbnInterface
title: IMbnInterface
author: windows-sdk-content
description: Represents a Mobile Broadband device.
old-location: mbn\imbninterface.htm
old-project: mbn
ms.assetid: 958bce42-4772-4706-8900-1f83c5d3d52b
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IMbnInterface, IMbnInterface interface [Microsoft Broadband Networks], IMbnInterface interface [Microsoft Broadband Networks],described, mbn.imbninterface, mbnapi/IMbnInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterface interface


## -description


Represents a Mobile Broadband device.

The properties and methods of <b>IMbnInterface</b> return the 
    state of the device. Applications should register for change event notifications by implementing 
    <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnInterface</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnInterface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnInterface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/919772f5-1e86-424c-b3de-079a03bbc8e5">GetConnection</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9d29a2a-f41b-4e20-b9ff-559dd39e1015">GetHomeProvider</a>
</td>
<td align="left" width="63%">
Gets the home provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfe8f638-ad17-4118-9c79-b7ebc81c726a">GetInterfaceCapability</a>
</td>
<td align="left" width="63%">
Gets the device capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbd37f0a-4245-415d-bd74-501aa4c7ade7">GetPreferredProviders</a>
</td>
<td align="left" width="63%">
Gets the list of preferred providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4236fd9d-292a-4840-b52e-c28c3e6eea10">GetReadyState</a>
</td>
<td align="left" width="63%">
Gets the ready state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9114a3ed-2dc9-4637-b3d5-9430d309e89b">GetSubscriberInformation</a>
</td>
<td align="left" width="63%">
Gets the subscriber information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/916c29ee-adb3-402c-b4f3-97b8977f44ac">GetVisibleProviders</a>
</td>
<td align="left" width="63%">
Gets the visible providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4ce2c10-627d-4cbe-a884-7bb8731c3bcf">InEmergencyMode</a>
</td>
<td align="left" width="63%">
Determines whether the device is in emergency mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72db3d85-b7f2-4dae-9637-b003df6e9cf5">ScanNetwork</a>
</td>
<td align="left" width="63%">
Scans the network to get a list of visible providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ea95b4a-07d9-40d6-bb82-091b49c965c4">SetPreferredProviders</a>
</td>
<td align="left" width="63%">
Updates the preferred providers.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnInterface</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9828567b-ef5e-44b7-90ce-1788cd8dd947">InterfaceID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The interface ID.

</td>
</tr>
</table> 


## -remarks



<b>IMbnInterface</b> objects are provided by calls to the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/hh439398">GetInterface</a> and 
     <a href="https://msdn.microsoft.com/library/windows/hardware/hh439475">GetInterfaces</a> methods of the 
     <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> interface.



