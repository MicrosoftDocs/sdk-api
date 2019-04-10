---
UID: NF:portabledeviceapi.IEnumPortableDeviceObjectIDs.Clone
title: IEnumPortableDeviceObjectIDs::Clone (portabledeviceapi.h)
author: windows-sdk-content
description: The Clone method duplicates the current IEnumPortableDeviceObjectIDs interface.
old-location: wpdsdk\ienumportabledeviceobjectids_clone.htm
tech.root: wpd_sdk
ms.assetid: 70287534-501f-480d-85ee-64049a0938fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Portable Devices SDK], Clone method [Windows Portable Devices SDK],IEnumPortableDeviceObjectIDs interface, IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],Clone method, IEnumPortableDeviceObjectIDs.Clone, IEnumPortableDeviceObjectIDs::Clone, IEnumPortableDeviceObjectIDsClone, portabledeviceapi/IEnumPortableDeviceObjectIDs::Clone, wpdsdk.ienumportabledeviceobjectids_clone
ms.topic: method
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
 - IEnumPortableDeviceObjectIDs.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPortableDeviceObjectIDs::Clone


## -description


The <b>Clone</b> method duplicates the current I<b>EnumPortableDeviceObjectIDs</b> interface.
      

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




<a href="https://msdn.microsoft.com/70287534-501f-480d-85ee-64049a0938fb">IEnumPortableDeviceObjectIDs</a>



<a href="https://msdn.microsoft.com/0e9a65cc-819c-494e-9c7c-8f5fec78a2ee">IEnumPortableDeviceObjectIDs Interface</a>
 

 

