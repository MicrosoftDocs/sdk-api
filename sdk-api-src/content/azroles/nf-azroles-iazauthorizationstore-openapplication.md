---
UID: NF:azroles.IAzAuthorizationStore.OpenApplication
title: IAzAuthorizationStore::OpenApplication (azroles.h)
description: Opens the IAzApplication object with the specified name.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","OpenApplication method","IAzAuthorizationStore interface [Security]","OpenApplication method","IAzAuthorizationStore.OpenApplication","IAzAuthorizationStore::OpenApplication","OpenApplication","OpenApplication method [Security]","OpenApplication method [Security]","AzAuthorizationStore object","OpenApplication method [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::OpenApplication","security.azauthorizationstore_openapplication"]
old-location: security\azauthorizationstore_openapplication.htm
tech.root: security
ms.assetid: 63215a9a-b739-4ba9-a760-a9968be9e017
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],OpenApplication method, IAzAuthorizationStore interface [Security],OpenApplication method, IAzAuthorizationStore.OpenApplication, IAzAuthorizationStore::OpenApplication, OpenApplication, OpenApplication method [Security], OpenApplication method [Security],AzAuthorizationStore object, OpenApplication method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::OpenApplication, security.azauthorizationstore_openapplication
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
 - IAzAuthorizationStore::OpenApplication
 - azroles/IAzAuthorizationStore::OpenApplication
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
 - AzAuthorizationStore.OpenApplication
 - IAzAuthorizationStore.OpenApplication
---

# IAzAuthorizationStore::OpenApplication


## -description

The <b>OpenApplication</b> method opens the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object with the specified name.

## -parameters

### -param bstrApplicationName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object to open.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppApplication [out]

A pointer to a pointer to the opened <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.