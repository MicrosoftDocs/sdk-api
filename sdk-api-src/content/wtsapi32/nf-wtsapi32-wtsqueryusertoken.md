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

# WTSQueryUserToken function


## -description


Obtains the primary access token of the logged-on user specified by the session ID. To call 
    this function successfully, the calling application must be running within the context of the 
    <a href="https://msdn.microsoft.com/692bceb6-f5bd-4b83-ab3b-ef8099dc84e1">LocalSystem account</a> and have the 
    <b>SE_TCB_NAME</b> privilege.
<div class="alert"><b>Caution</b>  <b>WTSQueryUserToken</b> is 
    intended for highly trusted services. Service providers must use caution that they do not leak user tokens when 
    calling this function. Service providers must close token handles after they have finished using them.</div><div> </div>

## -parameters




### -param SessionId [in]

A Remote Desktop Services session identifier. Any program running in the context of a service will have a 
       session identifier of zero (0). You can use the 
      <a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a> function to retrieve 
      the identifiers of all sessions on a specified RD Session Host server.

To be able to query information for another user's session, you need to have the Query Information 
       permission. For more information, see 
       <a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services 
       Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration 
       administrative tool.


### -param phToken [out]

If the function succeeds, receives a pointer to the token handle for the logged-on user. Note that you must 
      call the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close this 
      handle.


## -returns



If the function succeeds, the return value is a nonzero value, and the <i>phToken</i> 
       parameter points to the primary token of the user.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among other errors, 
       <b>GetLastError</b> can return one of the following 
       errors.




## -remarks



For information about primary tokens, see 
    <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">Access Tokens</a>. For more information about 
    account privileges, see 
    <a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services Permissions</a> 
    and <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Authorization Constants</a>.

See <a href="https://msdn.microsoft.com/692bceb6-f5bd-4b83-ab3b-ef8099dc84e1">LocalSystem account</a> for 
    information about the privileges associated with that account.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a>
 

 

