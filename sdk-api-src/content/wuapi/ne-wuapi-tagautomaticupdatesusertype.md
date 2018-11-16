---
UID: NE:wuapi.tagAutomaticUpdatesUserType
title: tagAutomaticUpdatesUserType
author: windows-sdk-content
description: Defines the type of user.
old-location: wua\automaticupdatesusertype.htm
tech.root: Wua_Sdk
ms.assetid: e18c7aa0-111b-4209-bc7f-e533a26d684c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AutomaticUpdatesUserType, AutomaticUpdatesUserType enumeration [Windows Update Agent], auutCurrentUser, auutLocalAdministrator, tagAutomaticUpdatesUserType, wua.automaticupdatesusertype, wuapi/AutomaticUpdatesUserType, wuapi/auutCurrentUser, wuapi/auutLocalAdministrator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
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
 - Wuapi.h
api_name:
 - AutomaticUpdatesUserType
product: Windows
targetos: Windows
req.typenames: AutomaticUpdatesUserType
req.redist: 
---

# tagAutomaticUpdatesUserType enumeration


## -description


Defines the type of user.


## -enum-fields




### -field auutCurrentUser

The context of the current user.


### -field auutLocalAdministrator

Any administrator on the local computer.


## -remarks



The AutomaticUpdatesUserType is used in conjunction with the <a href="https://msdn.microsoft.com/fbf36d9f-98c1-4b9d-b479-a9203b6ce952">IAutomaticUpdatesSettings2::CheckPermission</a> method.



