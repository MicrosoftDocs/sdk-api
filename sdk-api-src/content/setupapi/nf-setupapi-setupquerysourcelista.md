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

# SetupQuerySourceListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQuerySourceList</b> function queries the current list of installation sources. The list is built from the system and user-specific lists, and potentially overridden by a temporary list (see 
<a href="https://msdn.microsoft.com/6a37a56c-ae44-4a57-9307-90efcf025d1a">SetupSetSourceList</a>).


## -parameters




### -param Flags [in]

Specifies which list to query. This parameter can be any combination of the following values. 







#### SRCLIST_SYSTEM

Query the system list.



#### SRCLIST_USER

Query the per-user list.

<div class="alert"><b>Note</b>  If the system and the user lists are both retrieved, they are merged with those items in the system list that appear first.</div>
<div> </div>
<div class="alert"><b>Note</b>  If none of the preceding flags are specified, the entire current (merged) list is returned.</div>
<div> </div>




#### SRCLIST_NOSTRIPPLATFORM

Normally, all paths are stripped of a platform-specific component if it is the final component. For example, a path stored in the registry as f:\x86 is returned as f:\. If this flag is specified, the platform-specific component is not stripped.


### -param List [in, out]

Pointer to a variable in which this function returns a pointer to an array of sources. Use a null-terminated string. The caller must free this array with a call to 
<a href="https://msdn.microsoft.com/ac326a2c-df67-4a3e-9290-663f84027a48">SetupFreeSourceList</a>.


### -param Count [in, out]

Pointer to a variable in which this function returns the number of sources in the list.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/6a37a56c-ae44-4a57-9307-90efcf025d1a">SetupSetSourceList</a>
 

 

