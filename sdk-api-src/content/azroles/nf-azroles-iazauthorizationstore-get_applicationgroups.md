---
UID: NF:azroles.IAzAuthorizationStore.get_ApplicationGroups
title: IAzAuthorizationStore::get_ApplicationGroups (azroles.h)
description: Retrieves an IAzApplicationGroups object that is used to enumerate IAzApplicationGroup objects from the policy data. (IAzAuthorizationStore.get_ApplicationGroups)
helpviewer_keywords: ["ApplicationGroups property [Security]","ApplicationGroups property [Security]","AzAuthorizationStore object","ApplicationGroups property [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","ApplicationGroups property","IAzAuthorizationStore interface [Security]","ApplicationGroups property","IAzAuthorizationStore.ApplicationGroups","IAzAuthorizationStore.get_ApplicationGroups","IAzAuthorizationStore::ApplicationGroups","IAzAuthorizationStore::get_ApplicationGroups","azroles/IAzAuthorizationStore::ApplicationGroups","azroles/IAzAuthorizationStore::get_ApplicationGroups","get_ApplicationGroups","security.azauthorizationstore_applicationgroups"]
old-location: security\azauthorizationstore_applicationgroups.htm
tech.root: security
ms.assetid: 02bab92b-b234-4755-a4d3-f787fe46252d
ms.date: 12/05/2018
ms.keywords: ApplicationGroups property [Security], ApplicationGroups property [Security],AzAuthorizationStore object, ApplicationGroups property [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],ApplicationGroups property, IAzAuthorizationStore interface [Security],ApplicationGroups property, IAzAuthorizationStore.ApplicationGroups, IAzAuthorizationStore.get_ApplicationGroups, IAzAuthorizationStore::ApplicationGroups, IAzAuthorizationStore::get_ApplicationGroups, azroles/IAzAuthorizationStore::ApplicationGroups, azroles/IAzAuthorizationStore::get_ApplicationGroups, get_ApplicationGroups, security.azauthorizationstore_applicationgroups
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
 - IAzAuthorizationStore::get_ApplicationGroups
 - azroles/IAzAuthorizationStore::get_ApplicationGroups
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
 - IAzAuthorizationStore.ApplicationGroups
 - IAzAuthorizationStore.get_ApplicationGroups
 - AzAuthorizationStore.ApplicationGroups
---

# IAzAuthorizationStore::get_ApplicationGroups


## -description

The <b>ApplicationGroups</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroups">IAzApplicationGroups</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object.
