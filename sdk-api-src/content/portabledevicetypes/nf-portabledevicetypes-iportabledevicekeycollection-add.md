---
UID: NF:portabledevicetypes.IPortableDeviceKeyCollection.Add
title: IPortableDeviceKeyCollection::Add method
author: windows-driver-content
description: The Add method adds a property key to the collection.
old-location: wpdsdk\iportabledevicekeycollection_add.htm
old-project: wpd_sdk
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Add method [Windows Portable Devices SDK], Add method [Windows Portable Devices SDK], IPortableDeviceKeyCollection interface, Add,IPortableDeviceKeyCollection.Add, IPortableDeviceKeyCollection, IPortableDeviceKeyCollection interface [Windows Portable Devices SDK], Add method, IPortableDeviceKeyCollection::Add, IPortableDeviceKeyCollectionAdd, portabledevicetypes/IPortableDeviceKeyCollection::Add, wpdsdk.iportabledevicekeycollection_add
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
-	IPortableDeviceKeyCollection.Add
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceKeyCollection::Add method


## -description



The <b>Add</b> method adds a property key to the collection.




## -parameters




### -param Key [in]

A <b>REFPROPERTYKEY</b> to add to the collection. This method copies the key to the collection, so you can release the local variable after calling this method.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to add the key to the collection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd">IPortableDeviceKeyCollection Interface</a>



<a href="https://msdn.microsoft.com/7fbd6f65-366a-49ea-a680-be77ca0d64f2">Retrieving Content-Object Properties</a>



<a href="https://msdn.microsoft.com/e4e3b286-6330-4147-a367-57accf5beae6">Retrieving Properties for a Single Object</a>



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>
 

 

