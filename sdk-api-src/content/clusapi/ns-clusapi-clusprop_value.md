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

# CLUSPROP_VALUE structure


## -description


Describes the syntax and 
    length of a data value used in a <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a>. The 
    <b>CLUSPROP_VALUE</b> structure is used as a generic header in 
    all of the structures that describe data of a particular type, such as 
    <a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a> and 
    <a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>.


## -struct-fields




### -field Syntax


<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a> union that describes a 
      value.


### -field cbLength

Count of bytes in the data that follows this 
      <b>CLUSPROP_VALUE</b> structure.


## -remarks



The <b>CLUSPROP_VALUE</b> structure is used to describe the 
     format, type, and length of a data value in the following structures:

<ul>
<li>
<a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8230d356-0d5a-4859-ae03-c25d078684b3">CLUSPROP_DISK_NUMBER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/38400cce-d84a-4439-9dab-20102c1580ff">CLUSPROP_DISK_SIGNATURE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2c88e9db-f218-4b88-9bb0-607fd09e8d0b">CLUSPROP_FILETIME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aa214e43-cadc-4f06-8c98-e6a5b13258b8">CLUSPROP_LONG</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3c508ed6-eec8-4fa9-9ae7-9c8d7f4c8b98">CLUSPROP_MULTI_SZ</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b1343a04-b8bd-469a-a620-985eeb89401c">CLUSPROP_PARTITION_INFO_EX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dae7544d-31c0-4a4b-8acb-d652bae817dd">CLUSPROP_REQUIRED_DEPENDENCY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ec01908-3765-4e95-a9d3-fdf6daa5f64d">CLUSPROP_RESOURCE_CLASS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/449f297e-6207-446e-ac80-03145c44d671">CLUSPROP_RESOURCE_CLASS_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/30907886-0c86-4e8a-9a95-5b62f6ffff76">CLUSPROP_SCSI_ADDRESS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1db28e46-e5e0-4d99-b9a8-80c3f1534ca6">CLUSPROP_ULARGE_INTEGER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ba09290b-171b-45cf-a367-485f7322ebef">CLUSPROP_WORD</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a>



<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

