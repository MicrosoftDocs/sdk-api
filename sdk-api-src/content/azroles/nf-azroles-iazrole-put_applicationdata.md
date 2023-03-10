---
UID: NF:azroles.IAzRole.put_ApplicationData
title: IAzRole::put_ApplicationData (azroles.h)
description: The ApplicationData property of IAzRole sets or retrieves an opaque field that can be used by the application to store information. (Put)
helpviewer_keywords: ["ApplicationData property [Security]","ApplicationData property [Security]","AzRole object","ApplicationData property [Security]","IAzRole interface","AzRole object [Security]","ApplicationData property","IAzRole interface [Security]","ApplicationData property","IAzRole.ApplicationData","IAzRole.put_ApplicationData","IAzRole::ApplicationData","IAzRole::get_ApplicationData","IAzRole::put_ApplicationData","azroles/IAzRole::ApplicationData","azroles/IAzRole::get_ApplicationData","azroles/IAzRole::put_ApplicationData","put_ApplicationData","security.iazrole_applicationdata"]
old-location: security\iazrole_applicationdata.htm
tech.root: security
ms.assetid: 6cb85528-35b4-4fed-98bb-6209dd0af0fd
ms.date: 12/05/2018
ms.keywords: ApplicationData property [Security], ApplicationData property [Security],AzRole object, ApplicationData property [Security],IAzRole interface, AzRole object [Security],ApplicationData property, IAzRole interface [Security],ApplicationData property, IAzRole.ApplicationData, IAzRole.put_ApplicationData, IAzRole::ApplicationData, IAzRole::get_ApplicationData, IAzRole::put_ApplicationData, azroles/IAzRole::ApplicationData, azroles/IAzRole::get_ApplicationData, azroles/IAzRole::put_ApplicationData, put_ApplicationData, security.iazrole_applicationdata
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
 - IAzRole::put_ApplicationData
 - azroles/IAzRole::put_ApplicationData
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
 - IAzRole.ApplicationData
 - IAzRole.get_ApplicationData
 - IAzRole.put_ApplicationData
 - AzRole.ApplicationData
---

# IAzRole::put_ApplicationData


## -description

The <b>ApplicationData</b> property sets or retrieves an opaque field that can be used by the application to store information.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Important</b>  Policy administrators can read from and write to this property. Applications should not store data in the <b>ApplicationData</b> property that should not be available to the policy administrator.</div>
<div> </div>

