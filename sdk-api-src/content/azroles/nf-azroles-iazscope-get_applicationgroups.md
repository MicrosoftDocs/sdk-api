---
UID: NF:azroles.IAzScope.get_ApplicationGroups
title: IAzScope::get_ApplicationGroups
author: windows-sdk-content
description: Retrieves an IAzApplicationGroups object that is used to enumerate IAzApplicationGroup objects from the policy data.
old-location: security\iazscope_applicationgroups.htm
old-project: SecAuthZ
ms.assetid: a8c9cffa-aebb-4bb1-834b-338082a9c8de
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ApplicationGroups property [Security], ApplicationGroups property [Security],AzScope object, ApplicationGroups property [Security],IAzScope interface, AzScope object [Security],ApplicationGroups property, IAzScope interface [Security],ApplicationGroups property, IAzScope.ApplicationGroups, IAzScope.get_ApplicationGroups, IAzScope::ApplicationGroups, IAzScope::get_ApplicationGroups, azroles/IAzScope::ApplicationGroups, azroles/IAzScope::get_ApplicationGroups, get_ApplicationGroups, security.iazscope_applicationgroups
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzScope.ApplicationGroups
 - IAzScope.get_ApplicationGroups
 - AzScope.ApplicationGroups
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::get_ApplicationGroups


## -description


The <b>ApplicationGroups</b> property retrieves an <a href="https://msdn.microsoft.com/e96c4cae-0a0a-4ac4-805f-2042312f0267">IAzApplicationGroups</a> object that is used to enumerate <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.



