---
UID: NF:azroles.IAzApplication.get_ApplicationGroups
title: IAzApplication::get_ApplicationGroups
author: windows-sdk-content
description: Retrieves an IAzApplicationGroups object that is used to enumerate IAzApplicationGroup objects from the policy data.
old-location: security\iazapplication_applicationgroups.htm
tech.root: secauthz
ms.assetid: 163d07cc-ce45-4e41-b9f2-79c7d360b899
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ApplicationGroups property [Security], ApplicationGroups property [Security],AzApplication object, ApplicationGroups property [Security],IAzApplication interface, AzApplication object [Security],ApplicationGroups property, IAzApplication interface [Security],ApplicationGroups property, IAzApplication.ApplicationGroups, IAzApplication.get_ApplicationGroups, IAzApplication::ApplicationGroups, IAzApplication::get_ApplicationGroups, azroles/IAzApplication::ApplicationGroups, azroles/IAzApplication::get_ApplicationGroups, get_ApplicationGroups, security.iazapplication_applicationgroups
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
 - IAzApplication.ApplicationGroups
 - IAzApplication.get_ApplicationGroups
 - AzApplication.ApplicationGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::get_ApplicationGroups


## -description


The <b>ApplicationGroups</b> property retrieves an <a href="https://msdn.microsoft.com/e96c4cae-0a0a-4ac4-805f-2042312f0267">IAzApplicationGroups</a> object that is used to enumerate <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



