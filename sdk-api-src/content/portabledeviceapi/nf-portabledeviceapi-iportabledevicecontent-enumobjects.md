---
UID: NF:portabledeviceapi.IPortableDeviceContent.EnumObjects
title: IPortableDeviceContent::EnumObjects (portabledeviceapi.h)
description: The EnumObjects method retrieves an interface that is used to enumerate the immediate child objects of an object. It has an optional filter that can enumerate objects with specific properties.
helpviewer_keywords: ["EnumObjects","EnumObjects method [Windows Portable Devices SDK]","EnumObjects method [Windows Portable Devices SDK]","IPortableDeviceContent interface","IPortableDeviceContent interface [Windows Portable Devices SDK]","EnumObjects method","IPortableDeviceContent.EnumObjects","IPortableDeviceContent::EnumObjects","IPortableDeviceContentEnumObjects","portabledeviceapi/IPortableDeviceContent::EnumObjects","wpdsdk.iportabledevicecontent_enumobjects"]
old-location: wpdsdk\iportabledevicecontent_enumobjects.htm
tech.root: wpdsdk
ms.assetid: 72526019-58c9-4a18-a925-e0a900f3e35a
ms.date: 12/05/2018
ms.keywords: EnumObjects, EnumObjects method [Windows Portable Devices SDK], EnumObjects method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],EnumObjects method, IPortableDeviceContent.EnumObjects, IPortableDeviceContent::EnumObjects, IPortableDeviceContentEnumObjects, portabledeviceapi/IPortableDeviceContent::EnumObjects, wpdsdk.iportabledevicecontent_enumobjects
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
 - IPortableDeviceContent::EnumObjects
 - portabledeviceapi/IPortableDeviceContent::EnumObjects
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
 - IPortableDeviceContent.EnumObjects
---

# IPortableDeviceContent::EnumObjects


## -description

The <b>EnumObjects</b> method retrieves an interface that is used to enumerate the immediate child objects of an object. It has an optional filter that can enumerate objects with specific properties.

## -parameters

### -param dwFlags [in]

Currently ignored; specify zero.

### -param pszParentObjectID [in]

Pointer to a null-terminated string that specifies the ID of the parent. This can be an empty string (but not a <b>NULL</b> pointer) or the defined constant <b>WPD_DEVICE_OBJECT_ID</b> to indicate the device root.

### -param pFilter [in]

This parameter is ignored and should be set to <b>NULL</b>.

### -param ppEnum [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-ienumportabledeviceobjectids">IEnumPortableDeviceObjectIDs</a> interface that is used to enumerate the objects that are found. The caller must release this interface when it is done with it.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the required arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wpd_sdk/enumerating-content">Enumerating Content</a>



<a href="/windows/desktop/wpd_sdk/enumerating-service-content">Enumerating Service Content</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-enumobjects">IPortableDeviceContent</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>