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

# peer_application_registration_type_tag enumeration


## -description


The <b>PEER_APPLICATION_REGISTRATION_TYPE</b> enumeration defines the set of peer application registration flags.


## -enum-fields




### -field PEER_APPLICATION_CURRENT_USER

The application is available only to the current user account logged into the machine.


### -field PEER_APPLICATION_ALL_USERS

The application is available to all user accounts set on the machine.


## -remarks



"Peer application" defines the set of software applications or components available for use with the peer collaboration network. The peer collaboration network enables participants in the network to initiate usage of this application.

Applications with the same GUID and registered for the <b>current user</b>  take precedence over applications with that same GUID registered for <b>all users</b>.




## -see-also




<a href="https://msdn.microsoft.com/f72e372a-0d23-47f4-8518-1296ec81ce55">Collaboration API Enumerations</a>
 

 

