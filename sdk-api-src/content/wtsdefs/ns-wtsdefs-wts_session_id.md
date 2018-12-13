---
UID: NS:wtsdefs._WTS_SESSION_ID
title: WTS_SESSION_ID
author: windows-sdk-content
description: Contains a GUID that uniquely identifies a session.
old-location: termserv\wts_session_id.htm
tech.root: TermServ
ms.assetid: fe0714ec-c670-40b7-9808-2171abae79a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWTS_SESSION_ID, PWRDS_SESSION_ID, PWRDS_SESSION_ID structure pointer [Remote Desktop Services], PWTS_SESSION_ID, PWTS_SESSION_ID structure pointer [Remote Desktop Services], WRDS_SESSION_ID, WRDS_SESSION_ID structure [Remote Desktop Services], WTS_SESSION_ID, WTS_SESSION_ID structure [Remote Desktop Services], termserv.wts_session_id, wtsdefs/PWRDS_SESSION_ID, wtsdefs/PWTS_SESSION_ID, wtsdefs/WRDS_SESSION_ID, wtsdefs/WTS_SESSION_ID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Wtsdefs.h
api_name:
 - WTS_SESSION_ID
product: Windows
targetos: Windows
req.typenames: WTS_SESSION_ID, *PWTS_SESSION_ID
req.redist: 
---

# WTS_SESSION_ID structure


## -description


Contains a <b>GUID</b> that uniquely identifies a session.


## -struct-fields




### -field SessionUniqueGuid

A GUID that specifies the client connection.


### -field SessionId

An integer that specifies the session associated with the client connection.


## -remarks



This structure is used in the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/541bf463-9a4a-4237-8a61-1288ab1540cc">AuthenticateClientToSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6065e827-23a5-4150-bda5-999b7acede65">LogonNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5a545f66-7143-419d-9e0c-a96070472ce5">NotifySessionId</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/541bf463-9a4a-4237-8a61-1288ab1540cc">AuthenticateClientToSession</a>



<a href="https://msdn.microsoft.com/6065e827-23a5-4150-bda5-999b7acede65">LogonNotify</a>



<a href="https://msdn.microsoft.com/5a545f66-7143-419d-9e0c-a96070472ce5">NotifySessionId</a>



<a href="https://msdn.microsoft.com/45d17758-4554-42aa-aeb9-c8d4e7fc6bb7">Remote Desktop Protocol Provider Structures</a>
 

 

