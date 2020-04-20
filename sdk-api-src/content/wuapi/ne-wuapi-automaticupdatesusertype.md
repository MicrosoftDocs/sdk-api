---
UID: NE:wuapi.tagAutomaticUpdatesUserType
title: AutomaticUpdatesUserType (wuapi.h)
description: Defines the type of user.helpviewer_keywords: ["AutomaticUpdatesUserType","AutomaticUpdatesUserType enumeration [Windows Update Agent]","auutCurrentUser","auutLocalAdministrator","wua.automaticupdatesusertype","wuapi/AutomaticUpdatesUserType","wuapi/auutCurrentUser","wuapi/auutLocalAdministrator"]
old-location: wua\automaticupdatesusertype.htm
tech.root: Wua_Sdk
ms.assetid: e18c7aa0-111b-4209-bc7f-e533a26d684c
ms.date: 12/05/2018
ms.keywords: AutomaticUpdatesUserType, AutomaticUpdatesUserType enumeration [Windows Update Agent], auutCurrentUser, auutLocalAdministrator, wua.automaticupdatesusertype, wuapi/AutomaticUpdatesUserType, wuapi/auutCurrentUser, wuapi/auutLocalAdministrator
f1_keywords:
- wuapi/AutomaticUpdatesUserType
dev_langs:
- c++
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
targetos: Windows
req.typenames: AutomaticUpdatesUserType
req.redist: 
ms.custom: 19H1
---

# AutomaticUpdatesUserType enumeration


## -description


Defines the type of user.


## -enum-fields




### -field auutCurrentUser

The context of the current user.


### -field auutLocalAdministrator

Any administrator on the local computer.


## -remarks



The AutomaticUpdatesUserType is used in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission">IAutomaticUpdatesSettings2::CheckPermission</a> method.



