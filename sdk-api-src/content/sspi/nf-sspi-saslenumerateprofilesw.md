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

# SaslEnumerateProfilesW function


## -description


The <b>SaslEnumerateProfiles</b> function lists the packages that provide a SASL interface.


## -parameters




### -param ProfileList [out]

Pointer to a list of Unicode or ANSI strings that contain the names of the packages with SASL wrapper support.


### -param ProfileCount [out]

Pointer to an unsigned <b>LONG</b> value that contains the number of packages with SASL wrapper support.


## -returns



If the call is completed successfully, this function returns SEC_E_OK.

If the function fails, the return value is a nonzero error code.




## -remarks



The current list is maintained in the registry under <pre xml:space="preserve"><b>SYSTEM</b>
   <b>CurrentControlSet</b>
      <b>Control</b>
         <b>SecurityProviders</b>
            <b>SaslProfiles</b></pre>


A terminating <b>NULL</b> character is appended to the end of the list.



