---
UID: NF:azroles.IAzScope.get_ApplicationGroups
title: IAzScope::get_ApplicationGroups (azroles.h)
description: Retrieves an IAzApplicationGroups object that is used to enumerate IAzApplicationGroup objects from the policy data. (IAzScope.get_ApplicationGroups)
helpviewer_keywords: ["ApplicationGroups property [Security]","ApplicationGroups property [Security]","AzScope object","ApplicationGroups property [Security]","IAzScope interface","AzScope object [Security]","ApplicationGroups property","IAzScope interface [Security]","ApplicationGroups property","IAzScope.ApplicationGroups","IAzScope.get_ApplicationGroups","IAzScope::ApplicationGroups","IAzScope::get_ApplicationGroups","azroles/IAzScope::ApplicationGroups","azroles/IAzScope::get_ApplicationGroups","get_ApplicationGroups","security.iazscope_applicationgroups"]
old-location: security\iazscope_applicationgroups.htm
tech.root: security
ms.assetid: a8c9cffa-aebb-4bb1-834b-338082a9c8de
ms.date: 12/05/2018
ms.keywords: ApplicationGroups property [Security], ApplicationGroups property [Security],AzScope object, ApplicationGroups property [Security],IAzScope interface, AzScope object [Security],ApplicationGroups property, IAzScope interface [Security],ApplicationGroups property, IAzScope.ApplicationGroups, IAzScope.get_ApplicationGroups, IAzScope::ApplicationGroups, IAzScope::get_ApplicationGroups, azroles/IAzScope::ApplicationGroups, azroles/IAzScope::get_ApplicationGroups, get_ApplicationGroups, security.iazscope_applicationgroups
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
 - IAzScope::get_ApplicationGroups
 - azroles/IAzScope::get_ApplicationGroups
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
 - IAzScope.ApplicationGroups
 - IAzScope.get_ApplicationGroups
 - AzScope.ApplicationGroups
---

# IAzScope::get_ApplicationGroups


## -description

The <b>ApplicationGroups</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroups">IAzApplicationGroups</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.
