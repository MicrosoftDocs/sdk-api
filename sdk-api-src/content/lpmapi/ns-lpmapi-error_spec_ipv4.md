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

# Error_Spec_IPv4 structure


## -description


The 
<b>Error_Spec_IPv4</b> structure stores error code information for RSVP transmissions.


## -struct-fields




### -field errs_errnode

IP address of the node responsible for the error, in the form of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a> structure.


### -field errs_flags

Error flags. Must be one of the following:

<ul>
<li>ERROR_SPECF_InPlace</li>
<li>ERROR_SPECF_NotGuilty</li>
</ul>

### -field errs_code

Error code. Must be one of the following:

<ul>
<li>ERR_FORWARD_OK</li>
<li>ERR_Usage_globl</li>
<li>ERR_Usage_local</li>
<li>ERR_Usage_serv</li>
<li>ERR_global_mask</li>
</ul>

### -field errs_value

Error value.


## -see-also




<a href="https://msdn.microsoft.com/4d20cbb8-c29a-4c0c-bf06-532144da3e33">ERROR_SPEC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a>
 

 

