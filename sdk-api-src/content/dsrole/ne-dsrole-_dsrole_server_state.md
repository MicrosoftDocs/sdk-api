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

# _DSROLE_SERVER_STATE enumeration


## -description


The <b>DSROLE_SERVER_STATE</b> enumeration is used with the <a href="https://msdn.microsoft.com/c368d8d9-a91d-4013-880e-36a47d42a697">DSROLE_UPGRADE_STATUS_INFO</a> structure to indicate the role of a server.


## -enum-fields




### -field DsRoleServerUnknown

The server role is unknown.


### -field DsRoleServerPrimary

The server was, or is, a primary domain controller.


### -field DsRoleServerBackup

The server was, or is, a backup domain controller.


## -see-also




<a href="https://msdn.microsoft.com/c368d8d9-a91d-4013-880e-36a47d42a697">DSROLE_UPGRADE_STATUS_INFO</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

