---
UID: NF:portabledeviceapi.IEnumPortableDeviceObjectIDs.Reset
title: IEnumPortableDeviceObjectIDs::Reset
author: windows-sdk-content
description: The Reset method resets the enumeration sequence to the beginning.
old-location: wpdsdk\ienumportabledeviceobjectids_reset.htm
tech.root: wpd_sdk
ms.assetid: 506c138e-6836-458f-823c-68978f224625
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],Reset method, IEnumPortableDeviceObjectIDs.Reset, IEnumPortableDeviceObjectIDs::Reset, IEnumPortableDeviceObjectIDsReset, Reset, Reset method [Windows Portable Devices SDK], Reset method [Windows Portable Devices SDK],IEnumPortableDeviceObjectIDs interface, portabledeviceapi/IEnumPortableDeviceObjectIDs::Reset, wpdsdk.ienumportabledeviceobjectids_reset
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
 - IEnumPortableDeviceObjectIDs.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPortableDeviceObjectIDs::Reset


## -description


The <b>Reset</b> method resets the enumeration sequence to the beginning.
      


## -parameters






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




<a href="https://msdn.microsoft.com/0e9a65cc-819c-494e-9c7c-8f5fec78a2ee">IEnumPortableDeviceObjectIDs Interface</a>
 

 

