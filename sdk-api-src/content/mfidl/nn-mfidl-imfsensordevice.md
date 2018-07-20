---
UID: NN:mfidl.IMFSensorDevice
title: IMFSensorDevice
author: windows-sdk-content
description: Represents a sensor device that can belong to a sensor group, which is represented by the IMFSensorGroup interface. The term &#0034;device&#0034; in this context could refer to a physical device, a custom media source, or a frame provider.
old-location: mf\imfsensordevice.htm
old-project: medfound
ms.assetid: 061EF002-178E-42CA-9D32-7E1282297BA4
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFSensorDevice, IMFSensorDevice interface [Media Foundation], IMFSensorDevice interface [Media Foundation],described, mf.imfsensordevice, mfidl/IMFSensorDevice
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
 - IMFSensorDevice
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorDevice interface


## -description


Represents a sensor device that can belong to a sensor group, which is represented by the <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a> interface. The term "device" in this context could refer to a physical device, a custom media source, or a frame provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4F509D34-23C3-4034-8D89-0A2E0651F235">GetDeviceAttributes</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> for the sensor group. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90598DC7-A4FB-4C3F-A671-1549703AC9DB">GetDeviceId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier for the device. This value is currently unused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6714B5A8-83F2-44CD-B061-749EA6BFBF20">GetDeviceType</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the type of sensor device represented by the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags set for the sensor device. This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21594884-DAA5-450C-855D-E800FE164C5E">GetSensorDeviceMode</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the current sharing mode of the sensor device, which is either controller or shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DDBEB335-E6E3-4185-B7EF-90FABA9CDCE5">GetStreamAttributes</a>
</td>
<td align="left" width="63%">
Gets the stream attribute store with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C6A0C4E6-7939-42C1-A499-7C92D83CB418">GetStreamAttributesCount</a>
</td>
<td align="left" width="63%">
Gets the count of stream attribute stores for the sensor device. This number represents the number of total streams available for the device because every valid stream must have an attribute store that contains at least the stream ID and stream category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F9244454-DF1D-4A3D-8A63-830A8422AFA2">GetSymbolicLink</a>
</td>
<td align="left" width="63%">
Gets the symbolic link name of the sensor device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B0DC098-EA3B-4061-8191-C67BA54663A3">SetSensorDeviceMode</a>
</td>
<td align="left" width="63%">
Sets a value that specifies the sharing mode of the sensor device to either controller or shared.

</td>
</tr>
</table> 

