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

# tagGLOBALOPT_PROPERTIES enumeration


## -description


Identifies process-global options that you can set or query by using the <a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a> interface.


## -enum-fields




### -field COMGLB_EXCEPTION_HANDLING

Defines COM exception-handling behavior.


### -field COMGLB_APPID

Sets the AppID for the process.


### -field COMGLB_RPC_THREADPOOL_SETTING

Sets the thread-pool behavior of the RPC runtime in the process.


### -field COMGLB_RO_SETTINGS

Used for miscellaneous settings.


### -field COMGLB_UNMARSHALING_POLICY

Defines the policy that's applied in the <a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a> function.


### -field COMGLB_PROPERTIES_RESERVED1


### -field COMGLB_PROPERTIES_RESERVED2




## -remarks



The unmarshaling policy option <b>COMGLB_UNMARSHALING_POLICY</b> takes values from the <a href="https://msdn.microsoft.com/7F557290-7162-4B32-880B-9A445A083F91">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a>



<a href="https://msdn.microsoft.com/7F557290-7162-4B32-880B-9A445A083F91">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a>



<a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>
 

 

