---
UID: NE:objidlbase.tagGLOBALOPT_PROPERTIES
title: tagGLOBALOPT_PROPERTIES
author: windows-sdk-content
description: Identifies process-global options that you can set or query by using the IGlobalOptions interface.
old-location: com\globalopt_properties.htm
tech.root: com
ms.assetid: 210BAEAF-D6FF-46E0-A187-D89EBB655B9C
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: COMGLB_APPID, COMGLB_EXCEPTION_HANDLING, COMGLB_RO_SETTINGS, COMGLB_RPC_THREADPOOL_SETTING, COMGLB_UNMARSHALING_POLICY, GLOBALOPT_PROPERTIES, GLOBALOPT_PROPERTIES enumeration [COM], com.globalopt_properties, objidl/COMGLB_APPID, objidl/COMGLB_EXCEPTION_HANDLING, objidl/COMGLB_RO_SETTINGS, objidl/COMGLB_RPC_THREADPOOL_SETTING, objidl/COMGLB_UNMARSHALING_POLICY, objidl/GLOBALOPT_PROPERTIES, tagGLOBALOPT_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidlbase.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidl.h
api_name:
 - GLOBALOPT_PROPERTIES
product: Windows
targetos: Windows
req.typenames: GLOBALOPT_PROPERTIES
req.redist: 
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
 

 

