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

# IRDPSRAPIInvitationManager::CreateInvitation


## -description


Creates an invitation.


## -parameters




### -param bstrAuthString [in]

Type: <b>BSTR</b>

String to use for the authorization. The string is limited to 255 characters and must be unique for the session. If <b>NULL</b>, the method generates the string for you.


### -param bstrGroupName [in]

Type: <b>BSTR</b>

The name of the group. The string must be unique for the session. Applications typically use the group name to separate attendees into groups that can be granted different authorization levels.


### -param bstrPassword [in]

Type: <b>BSTR</b>

Password to use for authentication. The password is limited to 255 characters. You must provide the password to the viewer out-of-band from the ticket.


### -param AttendeeLimit [in]

Type: <b>long</b>

The maximum number of attendees.


### -param ppInvitation [out]

Type: <b>IRDPSRAPIInvitation**</b>

An <a href="https://msdn.microsoft.com/66cd8251-726a-4368-8da5-4d3f6899bdc8">IRDPSRAPIInvitation</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/300940ef-e8a6-4dd9-a078-d4325e20ae91">IRDPSRAPIInvitationManager</a>
 

 

