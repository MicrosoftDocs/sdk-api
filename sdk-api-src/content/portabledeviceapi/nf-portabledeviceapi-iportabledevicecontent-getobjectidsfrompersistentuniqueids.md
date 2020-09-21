---
UID: NF:portabledeviceapi.IPortableDeviceContent.GetObjectIDsFromPersistentUniqueIDs
title: IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs (portabledeviceapi.h)
description: The GetObjectIDsFromPersistentUniqueIDs method retrieves the current object ID of one or more objects, given their persistent unique IDs (PUIDs).
helpviewer_keywords: ["GetObjectIDsFromPersistentUniqueIDs","GetObjectIDsFromPersistentUniqueIDs method [Windows Portable Devices SDK]","GetObjectIDsFromPersistentUniqueIDs method [Windows Portable Devices SDK]","IPortableDeviceContent interface","IPortableDeviceContent interface [Windows Portable Devices SDK]","GetObjectIDsFromPersistentUniqueIDs method","IPortableDeviceContent.GetObjectIDsFromPersistentUniqueIDs","IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs","IPortableDeviceContentGetObjectIDsFromPersistentUniqueIDs","portabledeviceapi/IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs","wpdsdk.iportabledevicecontent_getobjectidsfrompersistentuniqueids"]
old-location: wpdsdk\iportabledevicecontent_getobjectidsfrompersistentuniqueids.htm
tech.root: wpdsdk
ms.assetid: ee2aa718-0616-44b8-a9c6-cc835636500c
ms.date: 12/05/2018
ms.keywords: GetObjectIDsFromPersistentUniqueIDs, GetObjectIDsFromPersistentUniqueIDs method [Windows Portable Devices SDK], GetObjectIDsFromPersistentUniqueIDs method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],GetObjectIDsFromPersistentUniqueIDs method, IPortableDeviceContent.GetObjectIDsFromPersistentUniqueIDs, IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs, IPortableDeviceContentGetObjectIDsFromPersistentUniqueIDs, portabledeviceapi/IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs, wpdsdk.iportabledevicecontent_getobjectidsfrompersistentuniqueids
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
 - IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs
 - portabledeviceapi/IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs
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
 - IPortableDeviceContent.GetObjectIDsFromPersistentUniqueIDs
---

# IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs


## -description

The <b>GetObjectIDsFromPersistentUniqueIDs</b> method retrieves the current object ID of one or more objects, given their persistent unique IDs (PUIDs).

## -parameters

### -param pPersistentUniqueIDs [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that contains one or more persistent unique ID (PUID) string values (type VT_LPWSTR).

### -param ppObjectIDs [out]

Pointer to an <b>IPortableDevicePropVariantCollection</b> interface pointer that contains the retrieved object IDs, as type <b>VT_LPWSTR</b>. The retrieved IDs will be in the same order as the submitted PUIDs; if a value could not be found, it is indicated by an empty string. The caller must release this interface when it is done with it.

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

## -remarks

Windows Portable Devices Object IDs are unique across the device, but may be different across sessions. An Object ID can change when the application reconnects to the device.
      

Certain applications, such as synchronization engines, require a way to identify the object across connection sessions. Every object has a WPD_OBJECT_PERSISTENT_UNIQUE_ID property, which indicates an identifier that is persistent across sessions. Applications can read and save this property in their initial session, by calling the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-properties">Properties</a> method.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/retrieving-an-object-identifier-from-a-persistent-unique-identifier">Retrieving an Object Identifier from a Persistent Unique Identifier</a>


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-an-object-identifier-from-a-persistent-unique-identifier">Retrieving an Object Identifier from a Persistent Unique Identifier</a>