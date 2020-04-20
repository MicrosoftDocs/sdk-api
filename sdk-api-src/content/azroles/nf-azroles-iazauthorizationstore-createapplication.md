---
UID: NF:azroles.IAzAuthorizationStore.CreateApplication
title: IAzAuthorizationStore::CreateApplication (azroles.h)
description: Creates an IAzApplication object with the specified name.helpviewer_keywords: ["AzAuthorizationStore object [Security]","CreateApplication method","CreateApplication","CreateApplication method [Security]","CreateApplication method [Security]","AzAuthorizationStore object","CreateApplication method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","CreateApplication method","IAzAuthorizationStore.CreateApplication","IAzAuthorizationStore::CreateApplication","azroles/IAzAuthorizationStore::CreateApplication","security.azauthorizationstore_createapplication"]
old-location: security\azauthorizationstore_createapplication.htm
tech.root: SecAuthZ
ms.assetid: ca6feb69-15cd-454a-a2b8-c75c4c6b38cd
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],CreateApplication method, CreateApplication, CreateApplication method [Security], CreateApplication method [Security],AzAuthorizationStore object, CreateApplication method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],CreateApplication method, IAzAuthorizationStore.CreateApplication, IAzAuthorizationStore::CreateApplication, azroles/IAzAuthorizationStore::CreateApplication, security.azauthorizationstore_createapplication
f1_keywords:
- azroles/AzAuthorizationStore.CreateApplication
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- AzAuthorizationStore.CreateApplication
- IAzAuthorizationStore.CreateApplication
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzAuthorizationStore::CreateApplication


## -description


The <b>CreateApplication</b> method creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object with the specified name.


## -parameters




### -param bstrApplicationName [in]

Name for the new <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppApplication [out]

A pointer to a pointer to the created <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">IAzApplication::Submit</a> method to persist any changes made by the returned object.

The returned <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object is an immediate child object of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object.



