---
UID: NF:portabledeviceapi.IEnumPortableDeviceObjectIDs.Skip
title: IEnumPortableDeviceObjectIDs::Skip
author: windows-driver-content
description: The Skip method skips a specified number of objects in the enumeration sequence.
old-location: wpdsdk\ienumportabledeviceobjectids_skip.htm
old-project: wpd_sdk
ms.assetid: a55b9ccc-8d6b-49e6-af3d-ad7915aa3abd
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IEnumPortableDeviceObjectIDs interface [Windows Portable Devices SDK],Skip method, IEnumPortableDeviceObjectIDs.Skip, IEnumPortableDeviceObjectIDs::Skip, IEnumPortableDeviceObjectIDsSkip, Skip, Skip method [Windows Portable Devices SDK], Skip method [Windows Portable Devices SDK],IEnumPortableDeviceObjectIDs interface, portabledeviceapi/IEnumPortableDeviceObjectIDs::Skip, wpdsdk.ienumportabledeviceobjectids_skip
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IEnumPortableDeviceObjectIDs.Skip
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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




<a href="https://msdn.microsoft.com/a55b9ccc-8d6b-49e6-af3d-ad7915aa3abd">IEnumPortableDeviceObjectIDs</a>



<a href="https://msdn.microsoft.com/0e9a65cc-819c-494e-9c7c-8f5fec78a2ee">IEnumPortableDeviceObjectIDs Interface</a>
 

 

