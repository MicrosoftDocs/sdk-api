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

# FAX_ACCESS_RIGHTS_ENUM enumeration


## -description


The <b>FAX_ACCESS_RIGHTS_ENUM</b> enumeration defines access rights to the fax server.


## -enum-fields




### -field farSUBMIT_LOW

The user can submit low-priority fax jobs. Users can view and manage their jobs in the fax server's queue and their messages in the outgoing fax archive.


### -field farSUBMIT_NORMAL

The user can submit normal-priority and low-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.


### -field farSUBMIT_HIGH

The user can submit low-priority, normal-priority, and high-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.


### -field farQUERY_JOBS

The user can view all incoming and outgoing jobs in the fax server queue.


### -field farMANAGE_JOBS

The user can manage all incoming and outgoing jobs in the fax server queue.


### -field farQUERY_CONFIG

The user can view the fax server configuration data.


### -field farMANAGE_CONFIG

The user can set the fax server configuration data.


### -field farQUERY_IN_ARCHIVE

The user can view all fax messages in the incoming archive.


### -field farMANAGE_IN_ARCHIVE

The user can manage all fax messages in the incoming archive.


### -field farQUERY_OUT_ARCHIVE

The user can view all fax messages in the outgoing archive.


### -field farMANAGE_OUT_ARCHIVE

The user can manage all fax messages in the outgoing archive.


## -see-also




<a href="https://msdn.microsoft.com/329c4bd1-6b92-4dbf-aaf9-2e8c89192fd6">IFaxSecurity::get_GrantedRights</a>
 

 

