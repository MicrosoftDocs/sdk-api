---
UID: NF:portabledevicetypes.IPortableDevicePropVariantCollection.ChangeType
title: IPortableDevicePropVariantCollection::ChangeType method
author: windows-driver-content
description: The ChangeType method converts all items in the collection to the specified VARTYPE.
old-location: wpdsdk\iportabledevicepropvariantcollection_changetype.htm
old-project: wpd_sdk
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ChangeType method [Windows Portable Devices SDK], ChangeType method [Windows Portable Devices SDK], IPortableDevicePropVariantCollection interface, ChangeType,IPortableDevicePropVariantCollection.ChangeType, IPortableDevicePropVariantCollection, IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], ChangeType method, IPortableDevicePropVariantCollection::ChangeType, IPortableDevicePropVariantCollectionChangeType, portabledevicetypes/IPortableDevicePropVariantCollection::ChangeType, wpdsdk.iportabledevicepropvariantcollection_changetype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledevicetypes.h
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
req.typenames: WPD_STREAM_UNITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDevicePropVariantCollection.ChangeType
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevicePropVariantCollection::ChangeType method


## -description



The <b>ChangeType</b> method converts all items in the collection to the specified VARTYPE.




## -parameters




### -param vt [in]

Specifies the <b>VARTYPE</b> to which you want to convert all items in the collection. Example types include VT_UI4 and VT_UI8.


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



If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.




## -see-also




<a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection Interface</a>
 

 

