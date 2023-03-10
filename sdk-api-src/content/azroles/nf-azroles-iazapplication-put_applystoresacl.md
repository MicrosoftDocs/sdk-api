---
UID: NF:azroles.IAzApplication.put_ApplyStoreSacl
title: IAzApplication::put_ApplyStoreSacl (azroles.h)
description: Sets or retrieves a value that indicates whether policy audits should be generated when the authorization store is modified. (IAzApplication.put_ApplyStoreSacl)
helpviewer_keywords: ["ApplyStoreSacl property [Security]","ApplyStoreSacl property [Security]","AzApplication object","ApplyStoreSacl property [Security]","IAzApplication interface","AzApplication object [Security]","ApplyStoreSacl property","IAzApplication interface [Security]","ApplyStoreSacl property","IAzApplication.ApplyStoreSacl","IAzApplication.put_ApplyStoreSacl","IAzApplication::ApplyStoreSacl","IAzApplication::get_ApplyStoreSacl","IAzApplication::put_ApplyStoreSacl","azroles/IAzApplication::ApplyStoreSacl","azroles/IAzApplication::get_ApplyStoreSacl","azroles/IAzApplication::put_ApplyStoreSacl","put_ApplyStoreSacl","security.iazapplication_applystoresacl"]
old-location: security\iazapplication_applystoresacl.htm
tech.root: security
ms.assetid: 722b0693-a11f-434a-a278-780619b0077a
ms.date: 12/05/2018
ms.keywords: ApplyStoreSacl property [Security], ApplyStoreSacl property [Security],AzApplication object, ApplyStoreSacl property [Security],IAzApplication interface, AzApplication object [Security],ApplyStoreSacl property, IAzApplication interface [Security],ApplyStoreSacl property, IAzApplication.ApplyStoreSacl, IAzApplication.put_ApplyStoreSacl, IAzApplication::ApplyStoreSacl, IAzApplication::get_ApplyStoreSacl, IAzApplication::put_ApplyStoreSacl, azroles/IAzApplication::ApplyStoreSacl, azroles/IAzApplication::get_ApplyStoreSacl, azroles/IAzApplication::put_ApplyStoreSacl, put_ApplyStoreSacl, security.iazapplication_applystoresacl
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
 - IAzApplication::put_ApplyStoreSacl
 - azroles/IAzApplication::put_ApplyStoreSacl
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
 - IAzApplication.ApplyStoreSacl
 - IAzApplication.get_ApplyStoreSacl
 - IAzApplication.put_ApplyStoreSacl
 - AzApplication.ApplyStoreSacl
---

# IAzApplication::put_ApplyStoreSacl


## -description

The <b>ApplyStoreSacl</b> property sets or retrieves a value that indicates whether policy audits should be generated when the authorization store is modified.

This property is read/write.

## -parameters

## -remarks

Policy audits are generated when the underlying policy store is modified. Both success and failure audits are requested.

This property controls policy auditing only for the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object and its child objects.
