---
UID: NN:mfidl.IMFSensorGroup
title: IMFSensorGroup (mfidl.h)
author: windows-sdk-content
description: Represents a group of sensor devices from which an IMFMediaSource can be created.
old-location: mf\imfsensorgroup.htm
tech.root: medfound
ms.assetid: 7CED3EF6-E844-4B3A-8181-CA44FC4675EC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSensorGroup, IMFSensorGroup interface [Media Foundation], IMFSensorGroup interface [Media Foundation],described, mf.imfsensorgroup, mfidl/IMFSensorGroup
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFSensorGroup"
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorGroup interface


## -description


Represents a group of sensor devices from which an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> can be created. The term "device" in this context could refer to a physical device, a custom media source, or a frame provider. A sensor group may actually contain multiple sensor devices, or it could contain only a single device, but it still behaves as a sensor group.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorGroup</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorGroup</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-createmediasource">CreateMediaSource</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> that virtualizes the sensor group. The term "device" in this context could refer to a physical device or a software media source. The source can represent a sensor group that actually contains multiple sensor devices, or it could contain only a single device, but still behaves as a sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-getdefaultsensordeviceindex">GetDefaultSensorDeviceIndex</a>
</td>
<td align="left" width="63%">
Retrieves the index of the default device in the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags set for the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-getsensordevice">GetSensorDevice</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a> corresponding to a device in the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-getsensordevicecount">GetSensorDeviceCount</a>
</td>
<td align="left" width="63%">
Gets the number of devices that are virtualized by the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-getsensorgroupattributes">GetSensorGroupAttributes</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> for the sensor group. The returned object is a live reference to the internal attribute store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-getsymboliclink">GetSymbolicLink</a>
</td>
<td align="left" width="63%">
Gets the symbolic link name of the sensor group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-setdefaultsensordeviceindex">SetDefaultSensorDeviceIndex</a>
</td>
<td align="left" width="63%">
Configures one of the devices in the sensor group as the default device.

</td>
</tr>
</table> 

