---
UID: NF:azroles.IAzAuthorizationStore.get_Applications
title: IAzAuthorizationStore::get_Applications (azroles.h)
description: Retrieves an IAzApplications object that is used to enumerate IAzApplication objects from the policy store.
helpviewer_keywords: ["Applications property [Security]","Applications property [Security]","AzAuthorizationStore object","Applications property [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","Applications property","IAzAuthorizationStore interface [Security]","Applications property","IAzAuthorizationStore.Applications","IAzAuthorizationStore.get_Applications","IAzAuthorizationStore::Applications","IAzAuthorizationStore::get_Applications","azroles/IAzAuthorizationStore::Applications","azroles/IAzAuthorizationStore::get_Applications","get_Applications","security.azauthorizationstore_applications"]
old-location: security\azauthorizationstore_applications.htm
tech.root: security
ms.assetid: 7475fe41-b2fc-4a2c-a0db-c8c00bcc3ba4
ms.date: 12/05/2018
ms.keywords: Applications property [Security], Applications property [Security],AzAuthorizationStore object, Applications property [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],Applications property, IAzAuthorizationStore interface [Security],Applications property, IAzAuthorizationStore.Applications, IAzAuthorizationStore.get_Applications, IAzAuthorizationStore::Applications, IAzAuthorizationStore::get_Applications, azroles/IAzAuthorizationStore::Applications, azroles/IAzAuthorizationStore::get_Applications, get_Applications, security.azauthorizationstore_applications
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
 - IAzAuthorizationStore::get_Applications
 - azroles/IAzAuthorizationStore::get_Applications
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
 - IAzAuthorizationStore.Applications
 - IAzAuthorizationStore.get_Applications
 - AzAuthorizationStore.Applications
---

# IAzAuthorizationStore::get_Applications


## -description

The <b>Applications</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplications">IAzApplications</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> objects from the policy store.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object.