---
UID: NN:mfidl.IMFSensorDevice
title: IMFSensorDevice (mfidl.h)
description: Represents a sensor device that can belong to a sensor group, which is represented by the IMFSensorGroup interface. The term &#0034;device&#0034; in this context could refer to a physical device, a custom media source, or a frame provider.
old-location: mf\imfsensordevice.htm
tech.root: medfound
ms.assetid: 061EF002-178E-42CA-9D32-7E1282297BA4
ms.date: 12/05/2018
ms.keywords: IMFSensorDevice, IMFSensorDevice interface [Media Foundation], IMFSensorDevice interface [Media Foundation],described, mf.imfsensordevice, mfidl/IMFSensorDevice
f1_keywords:
- mfidl/IMFSensorDevice
dev_langs:
- c++
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
- IMFSensorDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorDevice interface


## -description


Represents a sensor device that can belong to a sensor group, which is represented by the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a> interface. The term "device" in this context could refer to a physical device, a custom media source, or a frame provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getdeviceattributes">GetDeviceAttributes</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> for the sensor group. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getdeviceid">GetDeviceId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier for the device. This value is currently unused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getdevicetype">GetDeviceType</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the type of sensor device represented by the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags set for the sensor device. This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getsensordevicemode">GetSensorDeviceMode</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the current sharing mode of the sensor device, which is either controller or shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getstreamattributes">GetStreamAttributes</a>
</td>
<td align="left" width="63%">
Gets the stream attribute store with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getstreamattributescount">GetStreamAttributesCount</a>
</td>
<td align="left" width="63%">
Gets the count of stream attribute stores for the sensor device. This number represents the number of total streams available for the device because every valid stream must have an attribute store that contains at least the stream ID and stream category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getsymboliclink">GetSymbolicLink</a>
</td>
<td align="left" width="63%">
Gets the symbolic link name of the sensor device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-setsensordevicemode">SetSensorDeviceMode</a>
</td>
<td align="left" width="63%">
Sets a value that specifies the sharing mode of the sensor device to either controller or shared.

</td>
</tr>
</table> 

