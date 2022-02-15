---
UID: NF:portabledeviceapi.IEnumPortableDeviceObjectIDs.Clone
title: IEnumPortableDeviceObjectIDs::Clone (portabledeviceapi.h)
description: The Clone method duplicates the current IEnumPortableDeviceObjectIDs interface.
helpviewer_keywords: ["Clone","Clone method [Windows Portable Devices SDK]","Clone method [Windows Portable Devices SDK]","IEnumPortableDeviceObjectIDs interface","IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK]","Clone method","IEnumPortableDeviceObjectIDs.Clone","IEnumPortableDeviceObjectIDs::Clone","IEnumPortableDeviceObjectIDsClone","portabledeviceapi/IEnumPortableDeviceObjectIDs::Clone","wpdsdk.ienumportabledeviceobjectids_clone"]
old-location: wpdsdk\ienumportabledeviceobjectids_clone.htm
tech.root: wpdsdk
ms.assetid: 70287534-501f-480d-85ee-64049a0938fb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Portable Devices SDK], Clone method [Windows Portable Devices SDK],IEnumPortableDeviceObjectIDs interface, IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],Clone method, IEnumPortableDeviceObjectIDs.Clone, IEnumPortableDeviceObjectIDs::Clone, IEnumPortableDeviceObjectIDsClone, portabledeviceapi/IEnumPortableDeviceObjectIDs::Clone, wpdsdk.ienumportabledeviceobjectids_clone
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
 - IEnumPortableDeviceObjectIDs::Clone
 - portabledeviceapi/IEnumPortableDeviceObjectIDs::Clone
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
 - IEnumPortableDeviceObjectIDs.Clone
---

# IEnumPortableDeviceObjectIDs::Clone


## -description

The <b>Clone</b> method duplicates the current <b>IEnumPortableDeviceObjectIDs</b> interface.
      

<b>Not implemented in this release.</b>

## -parameters

### -param ppEnum [out]

Address of a variable that receives a pointer to an enumeration interface. The caller must release this interface when it is finished with the interface.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented in this release.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-ienumportabledeviceobjectids-clone">IEnumPortableDeviceObjectIDs</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-ienumportabledeviceobjectids">IEnumPortableDeviceObjectIDs Interface</a>