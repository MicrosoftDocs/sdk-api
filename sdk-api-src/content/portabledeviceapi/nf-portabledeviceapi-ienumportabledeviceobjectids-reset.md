---
UID: NF:portabledeviceapi.IEnumPortableDeviceObjectIDs.Reset
title: IEnumPortableDeviceObjectIDs::Reset (portabledeviceapi.h)
description: The Reset method resets the enumeration sequence to the beginning. (IEnumPortableDeviceObjectIDs.Reset)
helpviewer_keywords: ["IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK]","Reset method","IEnumPortableDeviceObjectIDs.Reset","IEnumPortableDeviceObjectIDs::Reset","IEnumPortableDeviceObjectIDsReset","Reset","Reset method [Windows Portable Devices SDK]","Reset method [Windows Portable Devices SDK]","IEnumPortableDeviceObjectIDs interface","portabledeviceapi/IEnumPortableDeviceObjectIDs::Reset","wpdsdk.ienumportabledeviceobjectids_reset"]
old-location: wpdsdk\ienumportabledeviceobjectids_reset.htm
tech.root: wpdsdk
ms.assetid: 506c138e-6836-458f-823c-68978f224625
ms.date: 12/05/2018
ms.keywords: IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],Reset method, IEnumPortableDeviceObjectIDs.Reset, IEnumPortableDeviceObjectIDs::Reset, IEnumPortableDeviceObjectIDsReset, Reset, Reset method [Windows Portable Devices SDK], Reset method [Windows Portable Devices SDK],IEnumPortableDeviceObjectIDs interface, portabledeviceapi/IEnumPortableDeviceObjectIDs::Reset, wpdsdk.ienumportabledeviceobjectids_reset
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
 - IEnumPortableDeviceObjectIDs::Reset
 - portabledeviceapi/IEnumPortableDeviceObjectIDs::Reset
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
 - IEnumPortableDeviceObjectIDs.Reset
---

# IEnumPortableDeviceObjectIDs::Reset


## -description

The <b>Reset</b> method resets the enumeration sequence to the beginning.



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
</table>

## -remarks

There is no guarantee that the same objects will be enumerated after this method is called. This is because objects that were enumerated previously might have been deleted or new objects might have been added.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-ienumportabledeviceobjectids">IEnumPortableDeviceObjectIDs Interface</a>
