---
UID: NF:azroles.IAzScope.put_ApplicationData
title: IAzScope::put_ApplicationData (azroles.h)
description: The ApplicationData property of IAzScope sets or retrieves an opaque field that can be used by the application to store information. (Put)
helpviewer_keywords: ["ApplicationData property [Security]","ApplicationData property [Security]","AzScope object","ApplicationData property [Security]","IAzScope interface","AzScope object [Security]","ApplicationData property","IAzScope interface [Security]","ApplicationData property","IAzScope.ApplicationData","IAzScope.put_ApplicationData","IAzScope::ApplicationData","IAzScope::get_ApplicationData","IAzScope::put_ApplicationData","azroles/IAzScope::ApplicationData","azroles/IAzScope::get_ApplicationData","azroles/IAzScope::put_ApplicationData","put_ApplicationData","security.iazscope_applicationdata"]
old-location: security\iazscope_applicationdata.htm
tech.root: security
ms.assetid: c54aaadb-0c4a-43f9-ac50-413ed190b365
ms.date: 12/05/2018
ms.keywords: ApplicationData property [Security], ApplicationData property [Security],AzScope object, ApplicationData property [Security],IAzScope interface, AzScope object [Security],ApplicationData property, IAzScope interface [Security],ApplicationData property, IAzScope.ApplicationData, IAzScope.put_ApplicationData, IAzScope::ApplicationData, IAzScope::get_ApplicationData, IAzScope::put_ApplicationData, azroles/IAzScope::ApplicationData, azroles/IAzScope::get_ApplicationData, azroles/IAzScope::put_ApplicationData, put_ApplicationData, security.iazscope_applicationdata
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
 - IAzScope::put_ApplicationData
 - azroles/IAzScope::put_ApplicationData
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
 - IAzScope.ApplicationData
 - IAzScope.get_ApplicationData
 - IAzScope.put_ApplicationData
 - AzScope.ApplicationData
---

# IAzScope::put_ApplicationData


## -description

The <b>ApplicationData</b> property sets or retrieves an opaque field that can be used by the application to store information.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Important</b>  Policy administrators can read from and write to this property. Applications should not store data in the <b>ApplicationData</b> property that should not be available to the policy administrator.</div>
<div> </div>

