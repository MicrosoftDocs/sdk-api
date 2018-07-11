---
UID: NN:mfidl.IMFSensorGroup
title: IMFSensorGroup
author: windows-sdk-content
description: Represents a group of sensor devices from which an IMFMediaSource can be created.
old-location: mf\imfsensorgroup.htm
old-project: medfound
ms.assetid: 7CED3EF6-E844-4B3A-8181-CA44FC4675EC
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFSensorGroup, IMFSensorGroup interface [Media Foundation], IMFSensorGroup interface [Media Foundation],described, mf.imfsensorgroup, mfidl/IMFSensorGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorGroup
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorGroup interface


## -description


Represents a group of sensor devices from which an <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> can be created. The term "device" in this context could refer to a physical device, a custom media source, or a frame provider. A sensor group may actually contain multiple sensor devices, or it could contain only a single device, but it still behaves as a sensor group.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C69A81E-7159-43AA-92EA-7B1EB4A7A681">CreateMediaSource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> that virtualizes the sensor group. The term "device" in this context could refer to a physical device or a software media source. The source can represent a sensor group that actually contains multiple sensor devices, or it could contain only a single device, but still behaves as a sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E82A83F7-E984-4353-8CED-E3B5EE28EB3D">GetDefaultSensorDeviceIndex</a>
</td>
<td align="left" width="63%">
Retrieves the index of the default device in the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags set for the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78924C45-9612-4B39-B9E2-C8D2DCCBED79">GetSensorDevice</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a> corresponding to a device in the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/687A4275-5963-486E-8D59-B1858D7E388D">GetSensorDeviceCount</a>
</td>
<td align="left" width="63%">
Gets the number of devices that are virtualized by the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4EFC4615-AD97-4F58-9BEE-63F965DF8DDE">GetSensorGroupAttributes</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> for the sensor group. The returned object is a live reference to the internal attribute store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F71CFD47-6D44-4288-A70E-70040D19DB2D">GetSymbolicLink</a>
</td>
<td align="left" width="63%">
Gets the symbolic link name of the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06E2E2DB-8361-49BB-9369-0D0C33DF0C32">SetDefaultSensorDeviceIndex</a>
</td>
<td align="left" width="63%">
Configures one of the devices in the sensor group as the default device.

</td>
</tr>
</table> 

