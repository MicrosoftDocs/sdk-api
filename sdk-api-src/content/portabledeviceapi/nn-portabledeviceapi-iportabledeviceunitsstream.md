---
UID: NN:portabledeviceapi.IPortableDeviceUnitsStream
title: IPortableDeviceUnitsStream (portabledeviceapi.h)
author: windows-sdk-content
description: The IPortableDeviceUnitsStream interface provides a way to operate, or seek, on a stream by using alternate units, such as frames or milliseconds.
old-location: wpdsdk\iportabledeviceunitsstream.htm
tech.root: wpd_sdk
ms.assetid: 4E9B2ECC-91D0-4D4F-980D-54AC88F3175D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceUnitsStream, IPortableDeviceUnitsStream interface [Windows Portable Devices SDK], IPortableDeviceUnitsStream interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceUnitsStream, wpdsdk.iportabledeviceunitsstream
ms.topic: interface
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceUnitsStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceUnitsStream interface


## -description


The <b>IPortableDeviceUnitsStream</b> interface provides a way to operate, or seek, on a stream by using alternate units, such as frames or milliseconds.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceUnitsStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceUnitsStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceUnitsStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F94D30C7-57A8-4CBB-B416-ABB8BEC26A6E">IPortableDeviceUnitsStream::SeekInUnits</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/F94D30C7-57A8-4CBB-B416-ABB8BEC26A6E">SeekInUnits</a> method performs a seek on a stream, based on alternate units.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

