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

# DeleteProfileA function


## -description


Deletes the user profile and all user-related settings from the specified computer. The caller must have administrative privileges to delete a user's profile.


## -parameters




### -param lpSidString [in]

Type: <b>LPCTSTR</b>

Pointer to a string that specifies the user 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>.


### -param lpProfilePath [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a string that specifies the profile path. If this parameter is <b>NULL</b>, the function obtains the path from the registry.


### -param lpComputerName [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a string that specifies the name of the computer from which the profile is to be deleted. If this parameter is <b>NULL</b>, the local computer name is used.
    
                        

<div class="alert"><b>Note</b>  As of Windows Vista, this parameter must be <b>NULL</b>. If it is not, this function fails with the error code ERROR_INVALID_PARAMETER.</div>
<div> </div>

## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>DeleteProfile</b> might fail when passed the security identifier (SID) of the local system account (S-1-5-18). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=200321">KB890212</a>.




## -see-also




<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

