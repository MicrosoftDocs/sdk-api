---
UID: NN:portabledeviceapi.IEnumPortableDeviceObjectIDs
title: IEnumPortableDeviceObjectIDs (portabledeviceapi.h)
author: windows-sdk-content
description: The IEnumPortableDeviceObjectIDs interface enumerates the objects on a portable device. Get this interface initially by calling IPortableDeviceContent::EnumObjects on a device.
old-location: wpdsdk\ienumportabledeviceobjectids.htm
tech.root: wpd_sdk
ms.assetid: 0e9a65cc-819c-494e-9c7c-8f5fec78a2ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumPortableDeviceObjectIDs, IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK], IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],described, IEnumPortableDeviceObjectIDsInterface, portabledeviceapi/IEnumPortableDeviceObjectIDs, wpdsdk.ienumportabledeviceobjectids
ms.topic: interface
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IEnumPortableDeviceObjectIDs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPortableDeviceObjectIDs interface


## -description


The <b>IEnumPortableDeviceObjectIDs</b> interface enumerates the objects on a portable device. Get this interface initially by calling <a href="https://msdn.microsoft.com/72526019-58c9-4a18-a925-e0a900f3e35a">IPortableDeviceContent::EnumObjects</a> on a device.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPortableDeviceObjectIDs</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPortableDeviceObjectIDs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPortableDeviceObjectIDs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecf4644f-299c-46e0-922c-16de35674222">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending operation on the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70287534-501f-480d-85ee-64049a0938fb">Clone</a>
</td>
<td align="left" width="63%">
Duplicates the current <b>IEnumPortableDeviceObjectIDs</b> interface.

<b>Not implemented in this release.</b>

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a850b86-aeba-44b7-a686-9f3652a4c4ba">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next one or more object IDs in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/506c138e-6836-458f-823c-68978f224625">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a55b9ccc-8d6b-49e6-af3d-ad7915aa3abd">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of objects in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

