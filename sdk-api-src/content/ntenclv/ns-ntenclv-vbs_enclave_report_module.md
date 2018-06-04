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

# VBS_ENCLAVE_REPORT_MODULE structure


## -description


Describes a module loaded for the enclave. The report contains one <b>VBS_ENCLAVE_REPORT_MODULE</b> structure for every module loaded for the enclave except the primary module for the enclave, which is described in the <b>EnclaveIdentity</b> member of the <a href="https://msdn.microsoft.com/90D6E8D2-191B-41D2-8C75-28A26462644B">VBS_ENCLAVE_REPORT</a> structure.


## -struct-fields




### -field Header

The variable data header for the report.


### -field UniqueId

The enclave unique identifier of the module.


### -field AuthorId

The author identifier of the module.


### -field FamilyId

The family identifier of the module.


### -field ImageId

The image identifier of the module.


### -field Svn

The security version number of the module.


### -field ModuleName

A NULL-terminated string that contains the name of the module as it was loaded into the enclave.


## -see-also




<a href="https://msdn.microsoft.com/90D6E8D2-191B-41D2-8C75-28A26462644B">VBS_ENCLAVE_REPORT</a>



<a href="https://msdn.microsoft.com/A0B02839-E8F4-45A1-B2BA-73E6EF9DA7C8">VBS_ENCLAVE_REPORT_VARDATA_HEADER</a>
 

 

