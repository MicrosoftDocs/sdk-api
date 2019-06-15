---
UID: NE:dsrole._DSROLE_SERVER_STATE
title: DSROLE_SERVER_STATE (dsrole.h)
author: windows-sdk-content
description: Used with the DSROLE_UPGRADE_STATUS_INFO structure to indicate the role of a server.
old-location: ad\dsrole_server_state.htm
tech.root: ad
ms.assetid: cd15aa25-7a73-475f-b163-30e5dc1f52bd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDSROLE_SERVER_STATE, DSROLE_SERVER_STATE, DSROLE_SERVER_STATE enumeration [Active Directory], DsRoleServerBackup, DsRoleServerPrimary, DsRoleServerUnknown, ad.dsrole_server_state, dsrole/DSROLE_SERVER_STATE, dsrole/DsRoleServerBackup, dsrole/DsRoleServerPrimary, dsrole/DsRoleServerUnknown"
ms.topic: enum
req.header: dsrole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Dsrole.h
api_name:
 - DSROLE_SERVER_STATE
product: Windows
targetos: Windows
req.typenames: DSROLE_SERVER_STATE, *PDSROLE_SERVER_STATE
req.redist: 
ms.custom: 19H1
---

# DSROLE_SERVER_STATE enumeration


## -description


The <b>DSROLE_SERVER_STATE</b> enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_upgrade_status_info">DSROLE_UPGRADE_STATUS_INFO</a> structure to indicate the role of a server.


## -enum-fields




### -field DsRoleServerUnknown

The server role is unknown.


### -field DsRoleServerPrimary

The server was, or is, a primary domain controller.


### -field DsRoleServerBackup

The server was, or is, a backup domain controller.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_upgrade_status_info">DSROLE_UPGRADE_STATUS_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
 

 

