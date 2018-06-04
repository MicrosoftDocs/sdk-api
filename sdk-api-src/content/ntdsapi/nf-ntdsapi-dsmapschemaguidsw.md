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

# DsMapSchemaGuidsW function


## -description


The <b>DsMapSchemaGuids</b> function converts GUIDs of directory service schema objects to their display names.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param cGuids [in]

Indicates the number of elements in <i>rGuids</i>.


### -param rGuids [in]

Pointer to an array of <b>GUID</b> values for the objects to be mapped.


### -param ppGuidMap [out]

Pointer to a variable that receives a pointer to an array of 
<a href="https://msdn.microsoft.com/8128f511-ebdc-479d-b99c-ed210c72d151">DS_SCHEMA_GUID_MAP</a> structures that contain the display names of the objects in <i>rGuids</i>. This array must be deallocated using 
<a href="https://msdn.microsoft.com/54d6acb9-5602-4996-a483-08534143bc0a">DsFreeSchemaGuidMap</a>.


## -returns



Returns a standard error code that includes the following values.




## -see-also




<a href="https://msdn.microsoft.com/8128f511-ebdc-479d-b99c-ed210c72d151">DS_SCHEMA_GUID_MAP</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/54d6acb9-5602-4996-a483-08534143bc0a">DsFreeSchemaGuidMap</a>
 

 

