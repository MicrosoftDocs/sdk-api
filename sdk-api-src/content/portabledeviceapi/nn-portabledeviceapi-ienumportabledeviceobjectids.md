---
UID: NN:portabledeviceapi.IEnumPortableDeviceObjectIDs
title: IEnumPortableDeviceObjectIDs (portabledeviceapi.h)
description: The IEnumPortableDeviceObjectIDs interface enumerates the objects on a portable device. Get this interface initially by calling IPortableDeviceContent::EnumObjects on a device.
helpviewer_keywords: ["IEnumPortableDeviceObjectIDs","IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK]","IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK]","described","IEnumPortableDeviceObjectIDsInterface","portabledeviceapi/IEnumPortableDeviceObjectIDs","wpdsdk.ienumportabledeviceobjectids"]
old-location: wpdsdk\ienumportabledeviceobjectids.htm
tech.root: wpdsdk
ms.assetid: 0e9a65cc-819c-494e-9c7c-8f5fec78a2ee
ms.date: 12/05/2018
ms.keywords: IEnumPortableDeviceObjectIDs, IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK], IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],described, IEnumPortableDeviceObjectIDsInterface, portabledeviceapi/IEnumPortableDeviceObjectIDs, wpdsdk.ienumportabledeviceobjectids
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumPortableDeviceObjectIDs
 - portabledeviceapi/IEnumPortableDeviceObjectIDs
dev_langs:
 - c++
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
---

# IEnumPortableDeviceObjectIDs interface


## -description

The <b>IEnumPortableDeviceObjectIDs</b> interface enumerates the objects on a portable device. Get this interface initially by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-enumobjects">IPortableDeviceContent::EnumObjects</a> on a device.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPortableDeviceObjectIDs</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumPortableDeviceObjectIDs</b> also has these types of members:
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
<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-ienumportabledeviceobjectids-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending operation on the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-ienumportabledeviceobjectids-clone">Clone</a>
</td>
<td align="left" width="63%">
Duplicates the current <b>IEnumPortableDeviceObjectIDs</b> interface.

<b>Not implemented in this release.</b>

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-ienumportabledeviceobjectids-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next one or more object IDs in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-ienumportabledeviceobjectids-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-ienumportabledeviceobjectids-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of objects in the enumeration sequence.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>