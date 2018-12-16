---
UID: NF:ntdsapi.DsMapSchemaGuidsW
title: DsMapSchemaGuidsW function
author: windows-sdk-content
description: Converts GUIDs of directory service schema objects to their display names.
old-location: ad\dsmapschemaguids.htm
tech.root: ad
ms.assetid: 439fff20-51eb-490d-a330-61d07f79c436
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DsMapSchemaGuids, DsMapSchemaGuids function [Active Directory], DsMapSchemaGuidsA, DsMapSchemaGuidsW, _glines_dsmapschemaguids, ad.dsmapschemaguids, ntdsapi/DsMapSchemaGuids, ntdsapi/DsMapSchemaGuidsA, ntdsapi/DsMapSchemaGuidsW
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsMapSchemaGuidsW (Unicode) and DsMapSchemaGuidsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsMapSchemaGuids
 - DsMapSchemaGuidsA
 - DsMapSchemaGuidsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/ms676283(v=VS.85).aspx">DS_SCHEMA_GUID_MAP</a> structures that contain the display names of the objects in <i>rGuids</i>. This array must be deallocated using 
<a href="https://msdn.microsoft.com/54d6acb9-5602-4996-a483-08534143bc0a">DsFreeSchemaGuidMap</a>.


## -returns



Returns a standard error code that includes the following values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms676283(v=VS.85).aspx">DS_SCHEMA_GUID_MAP</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/54d6acb9-5602-4996-a483-08534143bc0a">DsFreeSchemaGuidMap</a>
 

 

