---
UID: NF:azroles.IAzAuthorizationStore.get_ApplicationGroups
title: IAzAuthorizationStore::get_ApplicationGroups
author: windows-sdk-content
description: Retrieves an IAzApplicationGroups object that is used to enumerate IAzApplicationGroup objects from the policy data.
old-location: security\azauthorizationstore_applicationgroups.htm
tech.root: SecAuthZ
ms.assetid: 02bab92b-b234-4755-a4d3-f787fe46252d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ApplicationGroups property [Security], ApplicationGroups property [Security],AzAuthorizationStore object, ApplicationGroups property [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],ApplicationGroups property, IAzAuthorizationStore interface [Security],ApplicationGroups property, IAzAuthorizationStore.ApplicationGroups, IAzAuthorizationStore.get_ApplicationGroups, IAzAuthorizationStore::ApplicationGroups, IAzAuthorizationStore::get_ApplicationGroups, azroles/IAzAuthorizationStore::ApplicationGroups, azroles/IAzAuthorizationStore::get_ApplicationGroups, get_ApplicationGroups, security.azauthorizationstore_applicationgroups
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzAuthorizationStore.ApplicationGroups
 - IAzAuthorizationStore.get_ApplicationGroups
 - AzAuthorizationStore.ApplicationGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::get_ApplicationGroups


## -description


The <b>ApplicationGroups</b> property retrieves an <a href="https://msdn.microsoft.com/e96c4cae-0a0a-4ac4-805f-2042312f0267">IAzApplicationGroups</a> object that is used to enumerate <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.



