---
UID: NE:functiondiscoveryapi.tagSystemVisibilityFlags
title: SystemVisibilityFlags (functiondiscoveryapi.h)
author: windows-sdk-content
description: Determines the visibility of the function instance's data.
old-location: ncd\systemvisibilityflags_enum.htm
tech.root: FunDisc
ms.assetid: a3388293-150c-417a-a4a6-0d5020e0ae82
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SVF_SYSTEM, SVF_USER, SystemVisibilityFlags, SystemVisibilityFlags enumeration, functiondiscoveryapi/SVF_SYSTEM, functiondiscoveryapi/SVF_USER, functiondiscoveryapi/SystemVisibilityFlags, ncd.systemvisibilityflags_enum
ms.topic: enum
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
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
 - FunctionDiscoveryAPI.h
api_name:
 - SystemVisibilityFlags
product: Windows
targetos: Windows
req.typenames: SystemVisibilityFlags
req.redist: 
---

# SystemVisibilityFlags enumeration


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines the visibility of the function instance's data.


## -enum-fields




### -field SVF_SYSTEM

The function instance's data is available to all users on the system.


### -field SVF_USER

The function instance's data is accessible only to the current user.


## -remarks



All data operations and function instances are stored in HKEY_LOCAL_MACHINE. Access to a function instance or its data with system-wide visibility must be performed with Administrator access permissions. 



