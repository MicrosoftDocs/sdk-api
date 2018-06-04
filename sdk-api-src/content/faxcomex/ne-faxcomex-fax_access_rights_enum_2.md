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

# FAX_ACCESS_RIGHTS_ENUM_2 enumeration


## -description


Defines access rights on the fax server.


## -enum-fields




### -field far2SUBMIT_LOW

The user can submit low-priority fax jobs. Users can view and manage their jobs in the fax server's queue and their messages in the outgoing fax archive.


### -field far2SUBMIT_NORMAL

The user can submit normal-priority and low-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.


### -field far2SUBMIT_HIGH

The user can submit low-priority, normal-priority, and high-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.


### -field far2QUERY_OUT_JOBS

The user can query outgoing jobs belonging to all accounts, including other user's accounts.


### -field far2MANAGE_OUT_JOBS

The user can manage outgoing jobs belonging to all accounts, including other user's accounts.


### -field far2QUERY_CONFIG

The user can view and query the fax server's configuration data.


### -field far2MANAGE_CONFIG

The user can view and set the fax server's configuration data.


### -field far2QUERY_ARCHIVES

The user can query archived messages belonging to all accounts, including other user's accounts.


### -field far2MANAGE_ARCHIVES

The user can manage archived messages belonging to all accounts, including other user's accounts.


### -field far2MANAGE_RECEIVE_FOLDER

The user can manage all the messages in the server's receive folder. This includes the right to <a href="https://msdn.microsoft.com/ede1c31f-e53a-4ddc-ba25-6fcadadd513a">reassign</a> and delete messages.


## -see-also




<a href="https://msdn.microsoft.com/c7a839d9-d7d5-4942-8886-b1ca494c5842">IFaxSecurity2::GrantedRights</a>
 

 

