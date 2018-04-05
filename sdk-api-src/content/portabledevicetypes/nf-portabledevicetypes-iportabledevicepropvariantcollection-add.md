---
UID: NF:portabledevicetypes.IPortableDevicePropVariantCollection.Add
title: IPortableDevicePropVariantCollection::Add method
author: windows-driver-content
description: The Add method adds an item to the collection.
old-location: wpdsdk\iportabledevicepropvariantcollection_add.htm
old-project: wpd_sdk
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Add method [Windows Portable Devices SDK], Add method [Windows Portable Devices SDK], IPortableDevicePropVariantCollection interface, Add,IPortableDevicePropVariantCollection.Add, IPortableDevicePropVariantCollection, IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], Add method, IPortableDevicePropVariantCollection::Add, IPortableDevicePropVariantCollectionAdd, portabledevicetypes/IPortableDevicePropVariantCollection::Add, wpdsdk.iportabledevicepropvariantcollection_add
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
-	IPortableDevicePropVariantCollection.Add
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevicePropVariantCollection::Add method


## -description



The <b>Add</b> method adds an item to the collection.




## -parameters




### -param pValue [in]

Pointer to a new <b>PROPVARIANT</b> object to add to the collection. This method copies the <b>PROPVARIANT</b> to the collection, so you should release your local copy of the variable by calling <b>PropVariantClear</b> after calling this method.


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



When the VARTYPE for <i>pValue</i> is VT_VECTOR or VT_UI1, setting and retrieving a <b>NULL</b> or zero-sized buffer is not supported. For example, neither pValue.caub.pElems = <b>NULL</b> nor pValue.caub.cElems = 0 are allowed.



If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail. To change the collection type manually, call <a href="https://msdn.microsoft.com/b01b6205-c900-4b2e-810f-426e1e71a008">IPortableDevicePropVariantCollection::ChangeType</a>.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection Interface</a>



<a href="https://msdn.microsoft.com/5072d308-d376-4141-96df-dbef23fb9f9b">Moving Content on the Device</a>



<a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>
 

 

