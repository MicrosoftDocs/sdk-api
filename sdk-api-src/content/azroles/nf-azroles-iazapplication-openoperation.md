---
UID: NF:azroles.IAzApplication.OpenOperation
title: IAzApplication::OpenOperation (azroles.h)
description: Opens an IAzOperation object with the specified name.
helpviewer_keywords: ["AzApplication object [Security]","OpenOperation method","IAzApplication interface [Security]","OpenOperation method","IAzApplication.OpenOperation","IAzApplication::OpenOperation","OpenOperation","OpenOperation method [Security]","OpenOperation method [Security]","AzApplication object","OpenOperation method [Security]","IAzApplication interface","azroles/IAzApplication::OpenOperation","security.iazapplication_openoperation"]
old-location: security\iazapplication_openoperation.htm
tech.root: security
ms.assetid: 37dddf38-a79b-419f-891b-8da7dc2bdf42
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],OpenOperation method, IAzApplication interface [Security],OpenOperation method, IAzApplication.OpenOperation, IAzApplication::OpenOperation, OpenOperation, OpenOperation method [Security], OpenOperation method [Security],AzApplication object, OpenOperation method [Security],IAzApplication interface, azroles/IAzApplication::OpenOperation, security.iazapplication_openoperation
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
 - IAzApplication::OpenOperation
 - azroles/IAzApplication::OpenOperation
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
 - IAzApplication.OpenOperation
 - AzApplication.OpenOperation
---

# IAzApplication::OpenOperation


## -description

The <b>OpenOperation</b> method opens an <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name.

## -parameters

### -param bstrOperationName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object to open.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppOperation [out]

A pointer to a pointer to the opened <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.