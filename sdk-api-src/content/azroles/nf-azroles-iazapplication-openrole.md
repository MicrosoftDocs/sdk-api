---
UID: NF:azroles.IAzApplication.OpenRole
title: IAzApplication::OpenRole (azroles.h)
description: Opens an IAzRole object with the specified name. (IAzApplication.OpenRole)
helpviewer_keywords: ["AzApplication object [Security]","OpenRole method","IAzApplication interface [Security]","OpenRole method","IAzApplication.OpenRole","IAzApplication::OpenRole","OpenRole","OpenRole method [Security]","OpenRole method [Security]","AzApplication object","OpenRole method [Security]","IAzApplication interface","azroles/IAzApplication::OpenRole","security.iazapplication_openrole"]
old-location: security\iazapplication_openrole.htm
tech.root: security
ms.assetid: 483c5b08-2f40-4ba6-afa0-ede596df8495
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],OpenRole method, IAzApplication interface [Security],OpenRole method, IAzApplication.OpenRole, IAzApplication::OpenRole, OpenRole, OpenRole method [Security], OpenRole method [Security],AzApplication object, OpenRole method [Security],IAzApplication interface, azroles/IAzApplication::OpenRole, security.iazapplication_openrole
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
 - IAzApplication::OpenRole
 - azroles/IAzApplication::OpenRole
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
 - IAzApplication.OpenRole
 - AzApplication.OpenRole
---

# IAzApplication::OpenRole


## -description

The <b>OpenRole</b> method opens an <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name.

## -parameters

### -param bstrRoleName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object to open.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppRole [out]

A pointer to a pointer to the opened <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.
