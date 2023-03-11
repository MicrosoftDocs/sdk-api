---
UID: NF:azroles.IAzApplication.get_ApplicationGroups
title: IAzApplication::get_ApplicationGroups (azroles.h)
description: Retrieves an IAzApplicationGroups object that is used to enumerate IAzApplicationGroup objects from the policy data. (IAzApplication.get_ApplicationGroups)
helpviewer_keywords: ["ApplicationGroups property [Security]","ApplicationGroups property [Security]","AzApplication object","ApplicationGroups property [Security]","IAzApplication interface","AzApplication object [Security]","ApplicationGroups property","IAzApplication interface [Security]","ApplicationGroups property","IAzApplication.ApplicationGroups","IAzApplication.get_ApplicationGroups","IAzApplication::ApplicationGroups","IAzApplication::get_ApplicationGroups","azroles/IAzApplication::ApplicationGroups","azroles/IAzApplication::get_ApplicationGroups","get_ApplicationGroups","security.iazapplication_applicationgroups"]
old-location: security\iazapplication_applicationgroups.htm
tech.root: security
ms.assetid: 163d07cc-ce45-4e41-b9f2-79c7d360b899
ms.date: 12/05/2018
ms.keywords: ApplicationGroups property [Security], ApplicationGroups property [Security],AzApplication object, ApplicationGroups property [Security],IAzApplication interface, AzApplication object [Security],ApplicationGroups property, IAzApplication interface [Security],ApplicationGroups property, IAzApplication.ApplicationGroups, IAzApplication.get_ApplicationGroups, IAzApplication::ApplicationGroups, IAzApplication::get_ApplicationGroups, azroles/IAzApplication::ApplicationGroups, azroles/IAzApplication::get_ApplicationGroups, get_ApplicationGroups, security.iazapplication_applicationgroups
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication::get_ApplicationGroups
 - azroles/IAzApplication::get_ApplicationGroups
dev_langs:
 - c++
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
---

# IAzApplication::get_ApplicationGroups


## -description

The <b>ApplicationGroups</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroups">IAzApplicationGroups</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.
