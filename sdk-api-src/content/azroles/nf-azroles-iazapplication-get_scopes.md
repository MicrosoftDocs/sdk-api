---
UID: NF:azroles.IAzApplication.get_Scopes
title: IAzApplication::get_Scopes (azroles.h)
description: Retrieves an IAzScopes object that is used to enumerate IAzScope objects from the policy data.
helpviewer_keywords: ["AzApplication object [Security]","Scopes property","IAzApplication interface [Security]","Scopes property","IAzApplication.Scopes","IAzApplication.get_Scopes","IAzApplication::Scopes","IAzApplication::get_Scopes","Scopes property [Security]","Scopes property [Security]","AzApplication object","Scopes property [Security]","IAzApplication interface","azroles/IAzApplication::Scopes","azroles/IAzApplication::get_Scopes","get_Scopes","security.iazapplication_scopes"]
old-location: security\iazapplication_scopes.htm
tech.root: security
ms.assetid: cb56e48c-5c36-49f5-927e-417bfb59f940
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],Scopes property, IAzApplication interface [Security],Scopes property, IAzApplication.Scopes, IAzApplication.get_Scopes, IAzApplication::Scopes, IAzApplication::get_Scopes, Scopes property [Security], Scopes property [Security],AzApplication object, Scopes property [Security],IAzApplication interface, azroles/IAzApplication::Scopes, azroles/IAzApplication::get_Scopes, get_Scopes, security.iazapplication_scopes
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
 - IAzApplication::get_Scopes
 - azroles/IAzApplication::get_Scopes
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
 - IAzApplication.Scopes
 - IAzApplication.get_Scopes
 - AzApplication.Scopes
---

# IAzApplication::get_Scopes


## -description

The <b>Scopes</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazscopes">IAzScopes</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.