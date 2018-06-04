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

# CLUSCTL_USER_CODE macro


## -description


Generates a correctly 
    formatted user-defined control code. For more information on the bit layout of control codes, see 
    <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a>.


## -parameters




### -param Function

Value that specifies the operation code (bits 0–23) and, optionally, the access code 
     (bits 0–1) of the resulting control code. The operation code can be any 19-bit value chosen 
     by the caller. The access code (if specified) should be set to one of the following values.



#### 0 (CLUS_ACCESS_ANY)

The control code has no access requirements.



#### 1 (CLUS_ACCESS_READ)

Use of the control code requires read access.



#### 2 (CLUS_ACCESS_WRITE)

Use of the control code requires write access.


### -param Object

An 8-bit value that specifies the object code (bits 24–31) of the resulting control 
      code. For more information on the bit layout of control codes, see 
      <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a>. The 
      object code can be set to any value greater than <b>CLUS_OBJECT_USER</b> (128).


## -remarks



Do not pass bit-shifted values for <i>Function</i> or <i>Object</i>. The 
    macro performs the required bit shifts.

If no access code is specified, the control code will default to 
    <b>CLUS_ACCESS_ANY</b>.


#### Examples

See the example under 
     <a href="https://msdn.microsoft.com/dc1191d0-9364-40a3-abca-c59aa9f5b3aa">Creating Control Codes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/75544022-6c6b-4a04-83cc-427307eaf3ea">CLUSCTL_GET_ACCESS_MODE</a>



<a href="https://msdn.microsoft.com/0f1abfdd-e6b2-42a8-8c77-54590e3b3a89">CLUSCTL_GET_CONTROL_FUNCTION</a>



<a href="https://msdn.microsoft.com/b49c030e-fe7a-45cd-bbbf-0056763d827c">CLUSCTL_GET_CONTROL_OBJECT</a>
 

 

