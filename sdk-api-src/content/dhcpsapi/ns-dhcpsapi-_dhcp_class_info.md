---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _DHCP_CLASS_INFO structure


## -description


The <b>DHCP_CLASS_INFO</b> structure defines a DHCP option class.


## -struct-fields




### -field ClassName

Unicode string that contains the name of the class.


### -field ClassComment

Unicode string that contains a comment associated with the class.


### -field ClassDataLength

Specifies the size of <b>ClassData</b>, in bytes. When passing this structure into <a href="https://msdn.microsoft.com/c38a593f-60f0-41c7-83a8-bbec9b79dfac">DhcpGetClassInfo</a>, this value should be set to the size of the initialized buffer.


### -field IsVendor

Specifies whether or not this option class is a vendor-defined option class. If <b>TRUE</b>, it is a vendor class; if not, it is not a vendor class. Vendor-defined option classes can be used by DHCP clients that are configured to optionally identify themselves by their vendor type to the DHCP server when obtaining a lease.


### -field Flags

Specifies a bit flag that indicates whether or not the options are vendor-specific. If it is not, this parameter should be 0.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
</dl>
</td>
<td width="60%">
This flag should be set if the option is provided by a vendor.

</td>
</tr>
</table>
 


### -field ClassData

Pointer to a byte buffer that contains specific data for the class. When passing this structure into <a href="https://msdn.microsoft.com/c38a593f-60f0-41c7-83a8-bbec9b79dfac">DhcpGetClassInfo</a>, this buffer should be initialized to the anticipated size of the data to be returned.


### -field ClassData.size_is

 


### -field ClassData.size_is.ClassDataLength

 




## -see-also




<a href="https://msdn.microsoft.com/716beba3-cba2-406c-a41f-2f08b6a7dc5a">DHCP_CLASS_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/ae30baba-a2cd-4662-a62a-58b59d119dc4">DhcpCreateClass</a>



<a href="https://msdn.microsoft.com/c38a593f-60f0-41c7-83a8-bbec9b79dfac">DhcpGetClassInfo</a>



<a href="https://msdn.microsoft.com/4ee8897f-d49a-4b60-a26e-e7e11c088353">DhcpModifyClass</a>
 

 

