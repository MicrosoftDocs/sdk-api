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

# __MIDL___MIDL_itf_bits5_0_0000_0000_0003 structure


## -description


The <b>BITS_JOB_PROPERTY_VALUE</b> union provides the 
    property value of the BITS job based on the value of the 
    <a href="https://msdn.microsoft.com/4ED7419E-3435-4F12-B293-1FDC24F40D63">BITS_JOB_PROPERTY_ID</a> enumeration.


## -struct-fields




### -field Dword

This value is returned when using the enum property ID 
      <b>BITS_JOB_PROPERTY_ID_COST_FLAGS</b> and is applied as the 
      <a href="bits_job_transfer_policy.htm">transfer policy</a> on the BITS job.

This value is also used when using the <b>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</b> to specify the minimum notification interval.


### -field ClsID

This value is returned when using the enum property ID 
     <b>BITS_JOB_PROPERTY_NOTIFICATION_CLSID</b> and represents the CLSID of the callback object 
     to register with the BITS job.


### -field Enable

This value is returned when using the enum property ID 
     <b>BITS_JOB_PROPERTY_DYNAMIC_CONTENT</b> to specify whether the BITS job has dynamic 
      content. This value is also returned when using the enum property ID 
      <b>BITS_JOB_PROPERTY_HIGH_PERFORMANCE</b>  to specify whether to mark the BITS job as an optimized download.

This value is also used when using the <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b>  to specify whether the BITS job is in on demand or not.


### -field Uint64

This value is returned when using the enum property ID 
      <b>BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE</b> to represent the maximum allowed download size 
      of an optimized download.


### -field Target

This value is returned when using the enum property ID <b>BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS</b> to represent the intranet authentication target which is permitted to use stored credentials.


## -see-also




<a href="https://msdn.microsoft.com/4ED7419E-3435-4F12-B293-1FDC24F40D63">BITS_JOB_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/6B321E80-333A-49F3-B36F-18652F2C92FE">BITS_JOB_TRANSFER_POLICY</a>
 

 

