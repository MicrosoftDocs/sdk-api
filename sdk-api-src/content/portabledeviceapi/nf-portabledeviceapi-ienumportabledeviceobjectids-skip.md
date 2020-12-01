---
UID: NF:portabledeviceapi.IEnumPortableDeviceObjectIDs.Skip
title: IEnumPortableDeviceObjectIDs::Skip (portabledeviceapi.h)
description: The Skip method skips a specified number of objects in the enumeration sequence.
helpviewer_keywords: ["IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK]","Skip method","IEnumPortableDeviceObjectIDs.Skip","IEnumPortableDeviceObjectIDs::Skip","IEnumPortableDeviceObjectIDsSkip","Skip","Skip method [Windows Portable Devices SDK]","Skip method [Windows Portable Devices SDK]","IEnumPortableDeviceObjectIDs interface","portabledeviceapi/IEnumPortableDeviceObjectIDs::Skip","wpdsdk.ienumportabledeviceobjectids_skip"]
old-location: wpdsdk\ienumportabledeviceobjectids_skip.htm
tech.root: wpdsdk
ms.assetid: a55b9ccc-8d6b-49e6-af3d-ad7915aa3abd
ms.date: 12/05/2018
ms.keywords: IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],Skip method, IEnumPortableDeviceObjectIDs.Skip, IEnumPortableDeviceObjectIDs::Skip, IEnumPortableDeviceObjectIDsSkip, Skip, Skip method [Windows Portable Devices SDK], Skip method [Windows Portable Devices SDK],IEnumPortableDeviceObjectIDs interface, portabledeviceapi/IEnumPortableDeviceObjectIDs::Skip, wpdsdk.ienumportabledeviceobjectids_skip
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
 - IEnumPortableDeviceObjectIDs::Skip
 - portabledeviceapi/IEnumPortableDeviceObjectIDs::Skip
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
 - IEnumPortableDeviceObjectIDs.Skip
---

# IEnumPortableDeviceObjectIDs::Skip


## -description

The <b>Skip</b> method skips a specified number of objects in the enumeration sequence.

## -parameters

### -param cObjects [in]

The number of objects to skip.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified number of objects could not be skipped (for instance, if fewer than <i>cObjects</i> remained in the enumeration sequence).

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-ienumportabledeviceobjectids-skip">IEnumPortableDeviceObjectIDs</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-ienumportabledeviceobjectids">IEnumPortableDeviceObjectIDs Interface</a>