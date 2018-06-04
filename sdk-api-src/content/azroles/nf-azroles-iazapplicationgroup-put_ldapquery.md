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

# IAzApplicationGroup::put_LdapQuery


## -description


The <b>LdapQuery</b> property sets or retrieves the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Lightweight Directory Access Protocol</a> (LDAP) query used to define membership for an LDAP query application group.

This property is read/write.


## -parameters


## -remarks



This property is ignored unless the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property is AZ_GROUPTYPE_LDAP_QUERY. 

The maximum length of this property is 4,096 characters.



